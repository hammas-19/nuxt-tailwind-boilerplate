<template>
  <canvas ref="canvasRef" class="particle-canvas-left" />
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const canvasRef = ref(null)
let canvas = null
let ctx = null
let mousePos = null
let points = []
let animationId = null

// Fixed settings
const PARTICLE_COUNT = 40 // Less particles for smaller area
const MAX_DISTANCE = 150
const PARTICLE_COLOR = '226,114,91' // #E2725B in RGB
const PARTICLE_SPEED = 0.3
const MOUSE_INTERACTION_DISTANCE = 200

// Point constructor function
function createPoint() {
  return {
    x: (Math.random() * (canvas.width + MAX_DISTANCE)) - (MAX_DISTANCE / 2),
    y: (Math.random() * (canvas.height + MAX_DISTANCE)) - (MAX_DISTANCE / 2),
    vx: (Math.random() * PARTICLE_SPEED) - (PARTICLE_SPEED / 2),
    vy: (Math.random() * PARTICLE_SPEED) - (PARTICLE_SPEED / 2),
    dia: Math.random() * 2 + 1 // Smaller particles
  }
}

// Generate points
function generatePoints(amount) {
  points = []
  for (let i = 0; i < amount; i++) {
    points.push(createPoint())
  }
}

// Draw individual point
function draw(obj) {
  ctx.beginPath()
  ctx.fillStyle = `rgba(${PARTICLE_COLOR}, 0.7)` // More transparent
  if (obj.dia) {
    ctx.arc(obj.x, obj.y, obj.dia, 0, 2 * Math.PI)
  } else {
    ctx.arc(obj.x, obj.y, 1, 0, 2 * Math.PI)
  }
  ctx.closePath()
  ctx.fill()
}

// Update point position
function update(obj) {
  obj.x += obj.vx
  obj.y += obj.vy

  // Wrap around screen edges
  if (obj.x > canvas.width + (MAX_DISTANCE / 2)) {
    obj.x = -(MAX_DISTANCE / 2)
  } else if (obj.x < -(MAX_DISTANCE / 2)) {
    obj.x = canvas.width + (MAX_DISTANCE / 2)
  }

  if (obj.y > canvas.height + (MAX_DISTANCE / 2)) {
    obj.y = -(MAX_DISTANCE / 2)
  } else if (obj.y < -(MAX_DISTANCE / 2)) {
    obj.y = canvas.height + (MAX_DISTANCE / 2)
  }
}

// Handle collisions and draw connections
function collision(obj, dist) {
  for (let i = 0; i < points.length; i++) {
    // Don't interact with self
    if (obj !== points[i]) {
      const distance = Math.sqrt(
        Math.pow((obj.x - points[i].x), 2) + Math.pow((obj.y - points[i].y), 2)
      )

      if (distance < dist) {
        ctx.beginPath()
        ctx.strokeStyle = `rgba(${PARTICLE_COLOR}, ${0.4 * Math.pow((dist - distance) / dist, 3)})` // More subtle
        ctx.moveTo(obj.x, obj.y)
        ctx.lineTo(points[i].x, points[i].y)
        ctx.closePath()
        ctx.stroke()
      }
    }
  }
}

// Main animation loop
function animate() {
  ctx.clearRect(0, 0, canvas.width, canvas.height)

  // Handle mouse interactions
  if (mousePos) {
    collision(mousePos, MOUSE_INTERACTION_DISTANCE)
    draw(mousePos)
  }

  // Update and draw all points
  for (let i = 0; i < points.length; i++) {
    collision(points[i], MAX_DISTANCE)
    draw(points[i])
    update(points[i])
  }

  animationId = requestAnimationFrame(animate)
}

// Resize canvas to fit container
function resizeCanvas() {
  if (!canvas) return

  const container = canvas.parentElement
  canvas.width = container.offsetWidth
  canvas.height = container.offsetHeight

  // Regenerate points for new canvas size
  if (points.length > 0) {
    generatePoints(PARTICLE_COUNT)
  }
}

// Get mouse position relative to canvas
function getMousePos(cvs, evt) {
  const rect = cvs.getBoundingClientRect()
  return {
    x: evt.clientX - rect.left,
    y: evt.clientY - rect.top
  }
}

// Handle mouse movement
function handleMouseMove(evt) {
  mousePos = getMousePos(canvas, evt)
}

// Initialize animation
function init() {
  canvas = canvasRef.value
  if (!canvas) return

  ctx = canvas.getContext('2d')

  // Set up event listeners
  canvas.addEventListener('mousemove', handleMouseMove)
  window.addEventListener('resize', resizeCanvas)

  // Initialize
  resizeCanvas()
  generatePoints(PARTICLE_COUNT)
  animate()
}

// Cleanup function
function cleanup() {
  if (animationId) {
    cancelAnimationFrame(animationId)
  }
  if (canvas) {
    canvas.removeEventListener('mousemove', handleMouseMove)
  }
  window.removeEventListener('resize', resizeCanvas)
}

// Lifecycle hooks
onMounted(() => {
  init()
})

onUnmounted(() => {
  cleanup()
})
</script>

<style scoped>
.particle-canvas-left {
  position: absolute;
  /* NOT fixed - this stays in its container */
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
}
</style>