<template>
  <main class="main-container">
    <section
      class="relative bg-[#001323] h-[100vh] flex justify-center items-center"
    >
      <div
        class="anim1 absolute flex justify-center text-white gap-24 p-12 flex-col xl:flex-row"
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

      <div
        class="anim2 absolute flex justify-center text-white gap-24 p-12 flex-col xl:flex-row"
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

      <div
        class="anim3 absolute flex justify-center text-white gap-24 p-12 flex-col xl:flex-row"
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
  mounted() {
    let scaleTimeline = gsap.timeline({
      scrollTrigger: {
        trigger: '.main-container',
        start: 'top top',
        end: '+=8000',
        scrub: 1,
        pin: '.main-container',
        markers: true,
      },
    })

    scaleTimeline
      .from('.anim1', {
        scale: 3,
        opacity: 0,
      })
      .to('.anim1', {
        scale: 0,
        opacity: 0,
      })
      .from(
        '.anim2',
        {
          scale: 3,
          opacity: 0,
        },
        0.7
      )
      .to('.anim2', {
        scale: 0,
        opacity: 0,
      })
      .from(
        '.anim3',
        {
          scale: 3,
          opacity: 0,
        },
        1.3
      )
      .to('.anim3', {
        scale: 0,
        opacity: 0,
      })
  },
}
</script>
<style lang=""></style>
