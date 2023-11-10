<template>
  <main>
    <div class="panel1 h-[300px] bg-red-500">
      <div class="text">
        <h1>asd</h1>
        <p>asdasdsad</p>
      </div>
    </div>
    <div class="panel2 h-[500px] bg-orange-500"><p>asd</p></div>
    <div class="panel3 h-[450px] bg-green-500"><p>asd</p></div>
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
      trigger: '.panel1',
      start: 'top top',
      pin: '.text',
      pinSpacing: false,
    })
  },
}
</script>
