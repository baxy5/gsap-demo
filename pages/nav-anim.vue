<template>
  <main>
    <nav id="nav" class="fixed w-full p-5 text-white">
      <ul class="flex justify-end gap-8">
        <li>Home</li>
        <li>Projects</li>
        <li>Contact</li>
      </ul>
    </nav>
    <section id="aasd" class="h-[50vh] bg-[#001234]"></section>
    <section id="asd" class="h-[50vh]"></section>
    <section id="aasd" class="h-[50vh] bg-[#001234]"></section>
    <section id="asd" class="h-[50vh]"></section>
    <section id="aasd" class="h-[50vh] bg-[#001234]"></section>
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
    gsap.to('#nav', {
      scrollTrigger: {
        trigger: '#asd',
        markers: true,
        toggleActions: 'play none none reset',
        start: 'top top',
        end: 'bottom top',
      },
      color: '#001234',
    })
  },
}
</script>
