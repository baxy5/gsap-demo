<template>
  <main class="overflow-hidden bg-[#001323]">
    <Logo />
    <Container container="scale-container" child="scale" />
    <Container container="scale-container2" child="scale2" />
    <Container container="scale-container3" child="scale3" />
    <Hero /> 
    <Wow />
    <section class="h-[100vh]"><p class="text-white">asd</p></section>
  </main>
</template>
<script>
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/all'
import Logo from '~/components/Logo.vue'
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
    Logo,
  },
  mounted() {},
}
</script>
<style lang=""></style>
