<template>
  <main>
    <section
      class="bg-[#D3DEE5] w-full fixed flex justify-between p-4 font-bold z-[90]"
    >
      <img src="../assets/appic-logo-sotet.svg" />
      <p>Menu</p>
    </section>

    <section class="hero h-full w-full bg-[#D3DEE5] pt-12 pb-8">
      <div class="hero-content px-[1.5rem]">
        <h1 class="text-[2.5rem] text-[#FF4A31] font-[800]">Project title</h1>
        <p class="text-[1.375rem] text-[#0D283F] font-[800]">
          Short text about the project. What it is, what impact it has had. Who
          we worked with, maybe a few words about the partner. In 3-5 lines.
          Highlight the main point & make it interesting.
        </p>
        <div class="text-[#0D283F] mt-8">
          <p class="text-[1rem] uppercase font-[800] mb-4">Services</p>
          <ul class="flex gap-[0.5rem]">
            <li
              class="bg-white text-[0.75rem] font-[600] rounded-[6.25rem] flex items-center justify-center py-[0.25rem] px-[0.63rem]"
            >
              Product Design
            </li>
            <li
              class="bg-white text-[0.75rem] font-[600] rounded-[6.25rem] flex items-center justify-center py-[0.25rem] px-[0.63rem]"
            >
              Design System
            </li>
            <li
              class="bg-white text-[0.75rem] font-[600] rounded-[6.25rem] flex items-center justify-center py-[0.25rem] px-[0.63rem]"
            >
              Webdesign
            </li>
            <li
              class="bg-white text-[0.75rem] font-[600] rounded-[6.25rem] flex items-center justify-center py-[0.25rem] px-[0.63rem]"
            >
              App Design
            </li>
          </ul>
        </div>
        <div class="text-[#0D283F] mt-8">
          <p class="text-[1rem] uppercase font-[800] mb-4">Industries</p>
          <ul class="flex gap-[0.5rem]">
            <li
              class="bg-white text-[0.75rem] font-[600] rounded-[6.25rem] flex items-center justify-center py-[0.25rem] px-[0.63rem]"
            >
              Pharmacy
            </li>
            <li
              class="bg-white text-[0.75rem] font-[600] rounded-[6.25rem] flex items-center justify-center py-[0.25rem] px-[0.63rem]"
            >
              Retail
            </li>
          </ul>
        </div>
        <div class="text-[#0D283F] mt-8">
          <p class="text-[1rem] uppercase font-[800] mb-4">Technologies</p>
          <ul class="flex gap-[0.5rem]">
            <li
              class="bg-white text-[0.75rem] font-[600] rounded-[6.25rem] flex items-center justify-center py-[0.25rem] px-[0.63rem]"
            >
              Angular
            </li>
            <li
              class="bg-white text-[0.75rem] font-[600] rounded-[6.25rem] flex items-center justify-center py-[0.25rem] px-[0.63rem]"
            >
              Node
            </li>
          </ul>
        </div>
      </div>

      <div class="section1 h-[100vh] text-[#0D283F] bg-[#D3DEE5]">
        <img
          class="img ml:px-[4rem] bg-[#D3DEE5]"
          src="../assets/ps.jpg"
          alt=""
        />
        <div class="desc-container relative">
          <div class="absolute top-0 px-[1.5rem] ml:px-[4rem] pt-8">
            <div class="desc1">
              <h2 class="text-[#FF4A31] text-[1rem] font-[800] uppercase">
                key challenge to solve
              </h2>
              <p class="text-[1.375rem] font-[800] pt-4">
                To highlight the main challenges of the project (initial
                problems or problems encountered during the process), focusing
                on the main ones, so that it is clear to everyone what we had to
                solve.
              </p>
            </div>
          </div>
          <div class="absolute top-0 w-full px-[1.5rem] ml:px-[4rem] pt-8">
            <div class="desc2">
              <h2 class="text-[#FF4A31] text-[1rem] font-[800] uppercase">
                our process
              </h2>
              <ul class="text-[1.375rem] font-[800] pt-4 grid gap-4">
                <li>Discover</li>
                <li>Market research</li>
                <li>Business development</li>
                <li>Deliver</li>
              </ul>
            </div>
          </div>
          <div class="absolute top-0 w-full px-[1.5rem] ml:px-[4rem] pt-8">
            <div class="desc3">
              <h2 class="text-[#FF4A31] text-[1rem] font-[800] uppercase">
                result
              </h2>
              <p class="text-[1.375rem] font-[800] pt-4">
                We have developed a mobile competence center that supports agile
                delivery and decreases time to market, resulting in a fast and
                easily scalable mobile application.
              </p>
            </div>
          </div>
        </div>
        <div class="cards-container">
          <div
            class="relative flex flex-col justify-center items-center text-center pt-8"
          >
            <div
              class="box1 absolute top-0 text-[#001826] p-[3rem] bg-white rounded-[2rem] w-[19rem] flex items-center justify-center flex-col"
            >
              <p class="text-[3.5rem] font-[500] pb-[1.5rem]">4,4</p>
              <p class="text-[1.125rem] font-[600]">Based on 23 000</p>
              <p class="text-[1.125rem] font-[600]">Appstore review</p>
            </div>
            <div
              class="box2 absolute top-0 text-[#001826] p-[3rem] bg-white rounded-[2rem] w-[19rem] flex items-center justify-center flex-col"
            >
              <p class="text-[3.5rem] font-[500] pb-[1.5rem]">4,4</p>
              <p class="text-[1.125rem] font-[600]">Based on 23 000</p>
              <p class="text-[1.125rem] font-[600]">Appstore review</p>
            </div>
            <div
              class="box3 absolute top-0 text-[#001826] p-[3rem] bg-white rounded-[2rem] w-[19rem] flex items-center justify-center flex-col"
            >
              <p class="text-[3.5rem] font-[500] pb-[1.5rem]">4,4</p>
              <p class="text-[1.125rem] font-[600]">Based on 23 000</p>
              <p class="text-[1.125rem] font-[600]">Appstore review</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="h-[100vh]">asd</section>

    <!-- <section class="h-[100vh]">
      <p>
        “It was fun to break from our routine of building MVPs with early-stage
        startups to blend into a team of executives. Spoiler: we did just as
        good.”
      </p>
    </section> -->
  </main>
</template>
<script>
import gsap from 'gsap'
import _ScrollTrigger from 'gsap/ScrollTrigger'
import { ScrollTrigger } from 'gsap/all'

if (typeof window !== 'undefined') {
  gsap.registerPlugin(ScrollTrigger)
}
export default {
  mounted() {
    let heroAnimation = gsap.timeline({
      scrollTrigger: {
        trigger: '.hero',
        start: 'top top',
        pin: '.hero-content',
        pinSpacing: false,
        scrub: 1,
      },
    })

    heroAnimation
      .set('.section1', {
        y: '40px',
      })
      .to('.hero-content', {
        opacity: 0,
        display: 'hidden',
      })

    let imageDetailsSection = gsap.timeline({
      scrollTrigger: {
        trigger: '.section1',
        start: 'top top+=60px',
        end: '+=5500',
        pin: '.section1',
        scrub: 1,
        fastScrollEnd: true, // vegen gyorsabban eltünik
      },
    })

    imageDetailsSection
      .set(['.desc1', '.desc2', '.desc3'], {
        opacity: 0,
        y: 100,
      })
      .set(['.box1', '.box2', '.box3'], {
        opacity: 0,
        y: 200,
      })
      .to('.desc1', {
        opacity: 4,
        y: 0,
      })
      .to('.desc1', {
        opacity: 0,
      })
      .to('.desc2', {
        opacity: 4,
        y: 0,
      })
      .to('.desc2', {
        opacity: 0,
      })
      .to('.desc3', {
        opacity: 4,
        y: 0,
      })
      .to('.img', {
        y: '-100%',
      })
      .to(
        '.desc3',
        {
          y: -250,
        },
        '<'
      )
      .to('.box1', {
        opacity: 4,
        y: 30,
      })
      .to('.box1', {
        opacity: 0.6,
        scale: 0.6,
        color: 'transparent',
      })
      .to('.box2', {
        opacity: 4,
        y: 80,
      })
      .to('.box2', {
        opacity: 0.8,
        scale: 0.8,
        color: 'transparent',
      })
      .to('.box3', {
        opacity: 4,
        y: 130,
      })
  },
}
</script>

<style></style>
