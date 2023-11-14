<template>
  <main>
    <div class="h-[40vh]"></div>
    <section class="bg-[#001234] pb-[200px]">
      <div class="grid grid-cols-2 h-full w-full">
        <div class="w-full h-full main-container">
          <div class="box1 h-[100vh] flex justify-center items-center">
            <p class="text1 opacity-[0] translate-y-[75px] text-white">
              Predicting delivery with an advanced analytics model, straight
              from your pocket.
            </p>
          </div>
          <div class="box2 h-[100vh] flex justify-center items-center">
            <p class="text2 opacity-[0] translate-y-[75px] text-white">
              Predicting delivery with an advanced analytics model, straight
              from your pocket.
            </p>
          </div>
          <div class="box3 h-[100vh] flex justify-center items-center">
            <p class="text3 opacity-[0] translate-y-[75px] text-white">
              Predicting delivery with an advanced analytics model, straight
              from your pocket.
            </p>
          </div>
        </div>
        <div
          class="fixed-container w-full h-[100vh] flex justify-center items-center"
        >
          <img class="w-[550px] h-auto" src="../assets/ps.jpg" />
        </div>
      </div>
    </section>
    <div class="h-[30vh]"></div>
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
        trigger: '.main-container',
        pin: '.fixed-container',
        scrub: 2,
        start: 'top top',
        end: 'bottom bottom',
      },
    })

    let box1 = gsap.timeline({
      scrollTrigger: {
        trigger: '.box1',
        start: 'top top',
        end: 'bottom bottom',
        scrub: 2,
      },
    })

    box1.to('.text1', {
      opacity: 4,
      y: 0,
    })

    let box2 = gsap.timeline({
      scrollTrigger: {
        trigger: '.box2',
        start: 'top top',
        end: 'bottom bottom',
        scrub: 2,
      },
    })

    box2.to('.text2', {
      opacity: 4,
      y: 0,
    })

    let box3 = gsap.timeline({
      scrollTrigger: {
        trigger: '.box3',
        start: 'top top',
        end: 'bottom bottom',
        scrub: 2,
      },
    })

    box3.to('.text3', {
      opacity: 4,
      y: 0,
    })
  },
}
</script>
