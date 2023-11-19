<template lang="">
  <main>
    <section
      class="bg-[#001323] h-[100vh] flex justify-center items-center"
      :class="`${container}`"
    >
      <div
        class="flex justify-center text-white gap-24 p-12 flex-col xl:flex-row"
        :class="`${child}`"
      >
        <div class="w-full xl:w-[25rem]">
          <h1 class="text-[2.5rem] md:text-[3.5rem] font-bold">MOL</h1>
          <p class="text-[1rem] md:text-[2rem]">
            Short text about the project. What it is, what impact it has had.
            Who we worked with, maybe a few words about the partner. In 3-5
            lines. Highlight the main point & make it interesting.
          </p>
        </div>
        <div class="flex justify-center items-center lg:gap-8 xl:gap-0">
          <img src="../assets/voda-mobile.png" alt="v" />
          <img
            src="../assets/voda-mobile.png"
            alt="v"
            class="hidden md:block"
          />
          <img
            src="../assets/voda-mobile.png"
            alt="v"
            class="hidden lg:block"
          />
        </div>
      </div>
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
  props: ['container', 'child'],
  mounted() {
    let scaleTimeline = gsap.timeline({
      scrollTrigger: {
        trigger: '.' + this.container,
        start: 'top top',
        end: '+=1500',
        scrub: 1,
        pin: '.' + this.container,
        //pinSpacing: false,
      },
    })

    scaleTimeline
      .set('.' + this.child, {
        scale: 3,
        opacity: 0,
      })
      .to('.' + this.child, {
        scale: 1,
        opacity: 4,
      })
      .to('.' + this.child, {
        scale: 1,
        duration: 1,
      })
      .to('.' + this.child, {
        scale: 0,
        opacity: 0,
      })
  },
}
</script>
<style lang=""></style>
