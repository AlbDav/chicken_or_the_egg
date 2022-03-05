<template>
  <div>
	  <div ref="challenge" class="h-screen w-full grid grid-cols-2 items-center">
      <div class="px-5">
        <span class="text-6xl md:text-7xl">Every collection represents a challenge</span>
      </div>
      <div ref="challengeImg">
        <img class="object-cover" src="../static/Saly-36.png" alt="pistols" />
      </div>
    </div>
	  <div ref="team" class="h-screen w-full grid grid-cols-2 items-center">
      <div ref="teamImg">
        <img class="object-cover" src="../static/Saly-15.png" alt="pistols" />
      </div>
      <div class="text-right px-5">
        <span class="text-6xl md:text-7xl">Choose your team wisely</span>
      </div>
    </div>
	  <div ref="buy" class="h-screen w-full grid grid-cols-2 items-center">
      <div class="px-5">
        <div>
          <span class="text-6xl md:text-7xl">Buy an NFT to support your team!</span>
        </div>
        <div class="text-center pt-5">
          <button ref="buyButton" class="bg-custom-orange text-white rounded-md py-3 px-5 shadow-md text-2xl">Go to the current challenge!</button>
        </div>
      </div>
      <div ref="buyImg">
        <img class="object-cover" src="../static/Saly-10.png" alt="pistols" />
      </div>
    </div>
  </div>
</template>

<script>
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

export default {
  mounted() {
    gsap.registerPlugin(ScrollTrigger)

    const challenge = this.$refs.challenge
    const challengeImg = this.$refs.challengeImg

    const challengeTimeline = gsap.timeline({
      ease: 'Power2.easeIn',
      scrollTrigger: {
        trigger: challenge,
        start: 'top top+=25%',
        toggleActions: 'play reverse play reverse'
      },
    })

    challengeTimeline
      .from(challengeImg, { y: '100px', autoAlpha: 0, duration: 1 })

    const team = this.$refs.team
    const teamImg = this.$refs.teamImg

    const teamTimeline = gsap.timeline({
      ease: 'Power2.easeIn',
      scrollTrigger: {
        trigger: team,
        start: 'top top+=25%',
        toggleActions: 'play reverse play reverse'
      },
    })

    teamTimeline
      .from(teamImg, { y: '100px', autoAlpha: 0, duration: 1 })

    const buy = this.$refs.buy
    const buyImg = this.$refs.buyImg
    const buyButton = this.$refs.buyButton;

    const buyTimeline = gsap.timeline({
      ease: 'Power2.easeIn',
      scrollTrigger: {
        trigger: buy,
        start: 'top top+=25%',
        toggleActions: 'play reverse play reverse'
      },
    })

    buyTimeline
      .from(buyImg, { y: '100px', autoAlpha: 0, duration: 1 })
      .from(buyButton, { y: '50px', autoAlpha: 0, duration: 1 }, 0.5)
  },
}
</script>