<template>
  <div
    ref="whichSide"
    class="h-screen h-screen w-full flex flex-col justify-evenly items-center"
  >
    <div ref="which" class="text-white text-8xl md:text-9xl text-center">Which side</div>
    <div ref="hr" class="w-10/12 h-1 bg-white rounded-full" />
    <div ref="side" class="text-white text-8xl md:text-9xl text-center">are you on?</div>
  </div>
</template>

<script>
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

export default {
  mounted() {
    gsap.registerPlugin(ScrollTrigger)

    const whichSide = this.$refs.whichSide
    const which = this.$refs.which
    const hr = this.$refs.hr
    const side = this.$refs.side

    const entranceTimeline = gsap.timeline({
      ease: 'Power2.easeIn',
      scrollTrigger: {
        trigger: whichSide,
        start: 'top top+=25%',
        end: 'top top',
        scrub: true,
      },
    })

    entranceTimeline
      .from(which, { x: '-50%', autoAlpha: 0 })
      .from(hr, { width: '0px' }, 0)
      .from(side, { x: '50%', autoAlpha: 0 }, 0)

    const exitTimeline = gsap.timeline({
      ease: 'Power2.easeOut',
      scrollTrigger: {
        trigger: whichSide,
        start: 'bottom center+=35%',
        end: 'bottom center',
        scrub: true,
      },
    })

    exitTimeline
      .to(which, { x: '+50%', autoAlpha: 0 })
      .to(hr, { width: '0px' }, 0)
      .to(side, { x: '-50%', autoAlpha: 0 }, 0)
  },
}
</script>