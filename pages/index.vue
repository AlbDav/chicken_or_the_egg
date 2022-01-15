<template>
  <div class="bg-black">
    <div class="h-screen w-full"></div>
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
    );

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
    );

    gsap.set(section2, {clipPath: 'circle(0%)'});
  },
}
</script>
