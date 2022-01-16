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
    <div ref="section2" class="h-screen w-full bg-white">ciao</div>
    <div class="h-screen w-full"></div>
  </div>
</template>

<script>
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

export default {
  name: 'IndexPage',
  mounted() {
    gsap.registerPlugin(ScrollTrigger)

    const section2 = this.$refs.section2

    gsap.fromTo(
      section2,
      { clipPath: 'circle(0%)' },
      {
        clipPath: 'circle(100%)',
        ease: 'Power2.easeInOut',
        scrollTrigger: {
          trigger: section2,
          start: 'top top+=25%',
          end: 'top top',
          scrub: true,
        },
      }
    )

    gsap.fromTo(
      section2,
      { clipPath: 'circle(100%)' },
      {
        clipPath: 'circle(0%)',
        ease: 'Power2.easeInOut',
        scrollTrigger: {
          trigger: section2,
          start: 'bottom center+=25%',
          end: 'bottom center',
          scrub: true,
        },
      }
    )

    gsap.set(section2, { clipPath: 'circle(0%)' })
  },
}
</script>
