<template>
  <main>
    <div class="panel1 h-[100vh] bg-red-500">
      <div class="text">
        <h1>asd</h1>
        <p>asdasdsad</p>
      </div>
    </div>
    <div class="panel2 h-[700px] bg-orange-500"><p>asd</p></div>
    <div class="panel3 h-[850px] bg-green-500"><p>asd</p></div>
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
    ScrollTrigger.create({
      trigger: '.panel2',
      start: 'top top',
      pin: '.panel2',
      pinSpacing: false,
      markers: true,
    })
  },
}
</script>
