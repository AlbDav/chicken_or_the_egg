<template>
  <div class="bg-black">
    <div class="h-screen w-full relative">
      <div class="absolute z-10 h-full w-full flex items-center px-16">
        <div class="w-3/4">
          <h1 class=" text-white text-8xl -mt-16">
            Join the challenge with us!
          </h1>
          <button class="bg-white rounded-md p-3 mt-14">
              Okaaaaaaay let's go
          </button>
        </div>
      </div>
      <div class="absolute z-0 h-full w-full flex items-center justify-end px-16">
        <img class="h-1/2" src="../static/Saly-11.png" alt="rocket">
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
