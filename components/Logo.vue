<template>
  <main>
    <section
      class="appic-logo-container h-[100vh] bg-[#001323] flex justify-center items-center"
    >
      <img
        class="appic-logo"
        src="../assets/appic-logo.png"
        alt="a"
        height="150"
        width="150"
      />
    </section>
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
    // Landing logo animation
    gsap.set('.appic-logo', { opacity: 4 })
    gsap.to('.appic-logo', {
      opacity: 0,
      scrollTrigger: {
        trigger: '.appic-logo-container',
        scrub: true,
        end: '+=700',
        pin: '.appic-logo-container',
      },
    })
  },
}
</script>
