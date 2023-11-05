<template>
  <main class="h-[100vh] hero-container bg-[#001323] text-white p-10">
    <div class="h-full w-full flex flex-col justify-between">
      <div class="hero flex justify-between items-center">
        <img src="../assets/appic-logo.png" alt="" height="150" width="150" />
        <ul class="flex items-center gap-10">
          <li>our work</li>
          <li>services</li>
          <li>join us</li>
          <li>contact</li>
        </ul>
      </div>
      <div class="hero">
        <h1 class="text-bold text-7xl pb-4">
          digital future <br />
          built today
        </h1>
        <p>Mobile & web applications that make an impact.</p>
      </div>
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
        trigger: '.hero',
        pin: '.hero-container', // akkor Pinel amikor a "scroller-start" eléri a "start" vonalat, magyarán amikor elindul az animáció
        pinSpacing: false, // automatikusan rak annyi spacinget mind az "end" ebben az esetbel 1500px, ezzel kikapcsoljuk és nem lesz
        scrub: 2,
        start: 'top 50px',
        end: '+=1500',
      },
    })

    tl.set('.hero', { opacity: 0 })
    tl.to('.hero', {
      opacity: 1,
    })
    tl.to('.hero', { opacity: 0 })
  },
}
</script>
<style lang=""></style>
