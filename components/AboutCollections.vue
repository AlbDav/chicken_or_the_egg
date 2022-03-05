<template>
  <div ref="about" class="w-full bg-white">
	  <CallToAction />
  </div>
</template>

<script>
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

export default {
  mounted() {
    gsap.registerPlugin(ScrollTrigger)

    const about = this.$refs.about

    gsap.fromTo(
      about,
      { clipPath: 'circle(40%)' },
      {
        clipPath: 'circle(100%)',
        ease: 'Power2.easeInOut',
        scrollTrigger: {
          trigger: about,
          start: 'top center',
          end: 'top top',
          scrub: true,
        },
      }
    )

    gsap.fromTo(
      about,
      { clipPath: 'circle(100%)' },
      {
        clipPath: 'circle(40%)',
        ease: 'Power2.easeInOut',
        scrollTrigger: {
          trigger: about,
          start: 'bottom bottom',
          end: 'bottom center',
          scrub: true,
        },
      }
    )

    gsap.set(about, { clipPath: 'circle(0%)' })
  },
}
</script>