<template>
  <div class="bg-black">
    <div class="h-screen w-full relative flex flex-col-reverse justify-center">
      <div
        class="
          md:absolute
          md:z-10
		  h-1/2
          md:h-full
          w-full
          flex
		  flex-row
          items-center
          px-8
          md:px-16
		  text-center
		  md:text-left
        "
      >
        <div class="md:w-3/4">
          <h1 class="text-white text-6xl md:text-8xl -mt-16">
            Join the challenge with us!
          </h1>
          <div class="mt-8 md:mt-14 md:ml-10">
            <button
              class="bg-custom-orange text-white rounded-md py-3 px-5 mr-5"
            >
              Buy now!
            </button>
            <button class="bg-white rounded-md py-3 px-5">Learn more</button>
          </div>
        </div>
      </div>
      <div
        class="md:absolute md:z-0 h-1/2 md:h-full w-full flex items-end md:items-center justify-center md:justify-end px-16"
      >
        <img class="h-5/6 md:h-auto w-auto" src="../static/Saly-11.png" alt="rocket" />
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
