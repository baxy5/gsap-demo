<template>
  <main class="overflow-hidden bg-[#001323]">
    <!-- <section
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
    <Container container="scale-container" child="scale" />
    <Container container="scale-container2" child="scale2" />
    <Container container="scale-container3" child="scale3" /> -->
    <Hero />
    <Wow />
    <div class="h-[100vh]"></div>
    <div class="h-[100vh]"></div>
  </main>
</template>
<script>
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/all'
import Container from '~/components/Container.vue'
import Hero from '~/components/Hero.vue'
import Wow from '~/components/Wow.vue'

if (typeof window !== 'undefined') {
  gsap.registerPlugin(ScrollTrigger)
}
export default {
  components: {
    Container,
    Hero,
    Wow,
  },
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
<style lang=""></style>
