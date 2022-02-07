<template>
  <div class="bg-black">
    <div class="h-screen w-full relative">
      <div class="absolute z-10 h-full w-full flex flex-col-reverse md:flex-row items-center px-8 md:px-16">
        <div class="md:w-3/4">
          <h1 class="text-white text-6xl md:text-8xl -mt-16">
            Join the challenge with us!
          </h1>
          <div class="mt-14 ml-10">
            <button class="bg-custom-orange text-white rounded-md py-3 px-5 mr-5">Buy now!</button>
            <button class="bg-white rounded-md py-3 px-5">
              Learn more
            </button>
          </div>
        </div>
      </div>
      <div
        class="absolute z-0 h-full w-full flex items-center justify-end px-16"
      >
        <img class="h-1/2" src="../static/Saly-11.png" alt="rocket" />
      </div>
    </div>
    <WhichSide />
    <AboutCollections />
    <div class="h-screen w-full"></div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>
