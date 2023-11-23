<template>
  <main>
    <section
      class="bg-[#D3DEE5] w-full fixed flex justify-between p-4 font-bold z-[90]"
    >
      <p>Appic</p>
      <p>Menu</p>
    </section>

    <section class="hero h-full w-full bg-[#D3DEE5] px-[1.5rem] pt-12 pb-8">
      <div class="hero-content">
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
    </section>

    <section class="section1 h-[100vh] text-[#0D283F] bg-[#D3DEE5]">
      <img class="img md:px-[4rem]" src="../assets/ps.jpg" alt="" />
      <div class="desc-container relative">
        <div class="absolute px-[1.5rem] pt-8">
          <div class="desc1">
            <h2 class="text-[#FF4A31] text-[1rem] font-[800] uppercase">
              key challenge to solve
            </h2>
            <p class="text-[1.375rem] font-[800] pt-4">
              To highlight the main challenges of the project (initial problems
              or problems encountered during the process), focusing on the main
              ones, so that it is clear to everyone what we had to solve.
            </p>
          </div>
        </div>
        <div class="absolute w-full px-[1.5rem] pt-8">
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
      </div>
    </section>

    <section class="section2 text-[#0D283F] bg-[#D3DEE5] px-[1.5rem] pt-36">
      <div id="second-container" class="relative">
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
        <div
          class="flex flex-col justify-center items-center text-center pt-16"
        >
          <div
            class="box1 text-[#001826] p-[3rem] bg-white rounded-[2rem] w-[19rem] flex items-center justify-center flex-col"
          >
            <p class="text-[3.5rem] font-[500] pb-[1.5rem]">4,4</p>
            <p class="text-[1.125rem] font-[600]">Based on 23 000</p>
            <p class="text-[1.125rem] font-[600]">Appstore review</p>
          </div>
          <div
            class="box2 text-[#001826] p-[3rem] bg-white rounded-[2rem] w-[19rem] flex items-center justify-center flex-col"
          >
            <p class="text-[3.5rem] font-[500] pb-[1.5rem]">3,3</p>
            <p class="text-[1.125rem] font-[600]">Based on 23 000</p>
            <p class="text-[1.125rem] font-[600]">Appstore review</p>
          </div>
          <div
            class="box3 text-[#001826] p-[3rem] bg-white rounded-[2rem] w-[19rem] flex items-center justify-center flex-col"
          >
            <p class="text-[3.5rem] font-[500] pb-[1.5rem]">4,5</p>
            <p class="text-[1.125rem] font-[600]">Based on 23 000</p>
            <p class="text-[1.125rem] font-[600]">Appstore review</p>
          </div>
        </div>
      </div>
    </section>

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
    let test = gsap.timeline({
      scrollTrigger: {
        trigger: '.hero',
        start: 'top top',
        scrub: true,
      },
    })

    test.to('.hero-content', {
      opacity: 0,
      y: '100%',
    })

    // section 1 animation
    let tl = gsap.timeline({
      scrollTrigger: {
        trigger: '.section1',
        pin: '.section1',
        scrub: 1,
        start: 'top 56px',
      },
    })

    tl.set(['.desc1', '.desc2'], {
      opacity: 0,
      y: 120,
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
        y: -25,
      })
      .to(
        '.img',
        {
          opacity: 0,
          y: -25,
        },
        '<'
      )

    // section 2 animation
    let tl2 = gsap.timeline({
      scrollTrigger: {
        trigger: '.section1',
        pin: '.section2',
        pinSpacing: false,
        start: 'bottom bottom',
        scrub: 1,
        markers: true,
      },
    })

    tl2
      .set('#second-container', {
        opacity: 0,
        y: 120,
      })
      .set(['.box1', '.box2', '.box3'], {
        opacity: 0,
        y: 120,
      })
      .to('#second-container', {
        opacity: 4,
        y: 0,
      })
      .to('.box1', {
        y: 0,
        opacity: 4,
      })
      .to('.box1', {
        scale: 0.7,
        opacity: 0.7,
      })
  },
}
</script>
