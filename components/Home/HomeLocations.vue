<template>
  <div class="def-container mb-[92px]">
    <div class="grid lg:grid-cols-2 gap-7  justify-items-center">
      <div class="w-full bg-peachy hover:bg-boss transition-all md:rounded-4xl rounded-2xl relative">
        <div class=" absolute top-10 left-10 flex flex-col gap-4 text-white">
          <h4 class="md:text-6xl text-3xl">
            Dubai
          </h4>
          <p class="text-xl">United Arab Emirates</p>
        </div>
        <img src="/dub.png" class=" h-full object-cover" alt="">
      </div>
      <div class="flex flex-col w-full gap-7">
        <div
          class="overflow-hidden md:rounded-4xl rounded-2xl  w-full bg-peachy hover:bg-boss transition-all flex justify-end relative">
          <div class=" absolute top-10 left-10 flex flex-col gap-4 text-white">
            <h4 class="md:text-6xl text-3xl">
              New York
            </h4>
            <p class="text-xl">United States of America</p>
          </div>
          <img src="/ny.png" class=" max-h-[380px] h-full" alt="">
        </div>
        <div
          class="overflow-hidden md:rounded-4xl rounded-2xl  w-full bg-peachy hover:bg-boss transition-all flex justify-end relative">
          <div class=" absolute top-10 left-10 flex flex-col gap-4 text-white">
            <h4 class="md:text-6xl text-3xl">
              Karachi
            </h4>
            <p class="text-xl">Pakistan</p>
          </div>
          <img src="/khi.png" class=" max-h-[380px] h-full" alt="">
        </div>
      </div>
    </div>
  </div>
</template>