<template>
  <main class="bg-[#D3DEE5]">
    <div id="container">
      <div class="flex justify-between items-center p-52">
        <div class="w-[500px]">
          <h1 class="text-[3.5rem] font-bold text-orange-500">Project title</h1>
          <p class="text-[1rem] font-bold">
            Short text about the project. What it is, what impact it has had.
            Who we worked with, maybe a few words about the partner. In 3-5
            lines. Highlight the main point & make it interesting.
          </p>
        </div>
        <div class="translate-y-48">
          <p class="font-bold text-[1rem]">Services</p>
          <ul class="grid gap-4">
            <li class="bg-white rounded-full p-2">Product Design</li>
            <li class="bg-white rounded-full p-2">Design System</li>
            <li class="bg-white rounded-full p-2">Webdesign</li>
            <li class="bg-white rounded-full p-2">App Design</li>
          </ul>
        </div>
      </div>
      <div>
        <div class="pt-40 px-32 text-black flex gap-[4rem]">
          <div class="testimage">
            <img src="../assets/ps.jpg" alt="1" />
          </div>
          <div class="pt-56 w-[48rem]">
            <p class="parag text-lg font-bold">
              To highlight the main challenges of the project (initial problems
              or problems encountered during the process), focusing on the main
              ones, so that it is clear to everyone what we had to solve.
            </p>
            <p class="parag2 text-lg font-bold">
              2To highlight the main challenges of the project (initial problems
              or problems encountered during the process), focusing on the main
              ones, so that it is clear to everyone what we had to solve.
            </p>
            <div class="flex gap-20">
              <div class="textbox">
                <h1 class="text-xl text-orange-500 font-bold">Result</h1>
                <p class="text-xl font-bold">
                  We have developed a mobile competence center that supports
                  agile delivery and decreases time to market, resulting in a
                  fast and easily scalable mobile application.
                </p>
              </div>
              <div class="box">
                <div class="bg-white p-10 rounded-[2.5rem]">
                  <h1>XX</h1>
                  <p>Based on 23 000</p>
                  <p>Appstore review</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="h-[100vh]"></div>
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
    let paragTl = gsap.timeline({
      scrollTrigger: {
        trigger: '#container',
        scrub: 1,
        pin: '#container',
        pinSpacer: false,
        markers: true,
        start: 'bottom bottom',
        end: () => innerHeight * 10,
      },
    })

    paragTl
      .set('.parag', {
        y: 100,
        x: -300,
        opacity: 0,
      })
      .set('.parag2', {
        y: 100,
        x: -300,
        opacity: 0,
      })
      .set('.textbox', {
        opacity: 0,
        y: 200,
        x: -700,
      })
      .set('.box', {
        opacity: 0,
        x: -600,
        y: 200,
      })
      .to('.parag', {
        y: -100,
        opacity: 4,
      })
      .to('.parag', {
        y: -500,
        opacity: 0,
      })
      .to('.parag2', {
        y: -100,
        opacity: 4,
      })
      .to('.parag2', {
        opacity: 0,
      })
      .to('.testimage', {
        clipPath: 'polygon(0 0, 100% 0, 100% 100%, 0 100%)',
        x: 300,
        ease: 'expo.out',
        duration: 5,
      })
      .to('.testimage', {
        opacity: 0,
        duration: 4,
      })
      .to('.textbox', {
        y: -400,
        opacity: 4,
      })
      .to('.box', {
        y: -400,
        opacity: 4,
      })

    gsap.set('.testimage', {
      clipPath: 'polygon(0 0, 100% 0, 100% 100%, 0 100%)',
      ease: 'expo.out',
      duration: 5,
    })
    gsap.to('.testimage', {
      scrollTrigger: {
        trigger: '.testimage',
        scrub: true,
      },
      clipPath: 'polygon(0 0, 60% 0, 60% 100%, 0 100%)',
      ease: 'expo.out',
      duration: 5,
    })
  },
}
</script>
<style lang=""></style>
