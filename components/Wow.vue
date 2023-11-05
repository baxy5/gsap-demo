<template>
  <main>
    <div
      id="container"
      class="relative h-[100vh] w-full flex justify-center items-center"
    >
    <p class="text-anim text-white text-8xl">We love to wow</p>
    <img class="text-anim absolute top-0 right-0" src="../assets/landing-top.png" />
    <img class="text-anim absolute top-0 left-0" src="../assets/landing-top-left.png" />
    <img class="text-anim absolute bottom-0 right-[50%]" src="../assets/landing-bottom.png" />
    </div>
  </main>
</template>
<script>
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/all'

if (typeof window !== 'undefined') {
  gsap.registerPlugin(ScrollTrigger)
}

export default {
  mounted() {
    let tl = gsap.timeline({
      scrollTrigger: {
        trigger: '.text-anim',
        scrub: 1,
        pin: '#container',
        start: 'center center',
      },
    })

    tl.from('.text-anim', {
      scale: 30,
      opacity: 0,
    }).to('.text-anim', {
      scale: 0,
      opacity: 0,
    })
  },
}
</script>
