<template>
  <div
    class="
      h-screen
      w-full
      relative
      flex flex-col-reverse
      justify-center
      box-border
      pt-20
    "
  >
    <div
      class="
        absolute z-10
        h-full
        w-full
        flex flex-row
        items-center
        px-8
        md:px-16
        text-left
      "
    >
      <div class="md:w-3/4">
        <h1 class="text-white text-6xl md:text-8xl -mt-16 title">
          Are you ready to join the challenge?
        </h1>
        <div class="mt-20 md:mt-14 md:ml-10 flex justify-center md:justify-start">
          <button class="bg-custom-orange text-white rounded-md py-3 px-5 mr-5 shadow-md text-xl">
            I'm ready!
          </button>
          <button class="bg-white rounded-md py-3 px-5 shadow-md text-xl">Tell me more</button>
        </div>
      </div>
    </div>
    <div
      class="
        absolute z-0
        h-full
        w-full
        flex
        items-center
        justify-end
        md:px-16
      "
    >
      <img class="object-cover" src="../static/Saly-11.png" alt="rocket" />
    </div>
  </div>
</template>

<style scoped>
.title {
  text-shadow: black 0px 0px 5px;
}
</style>