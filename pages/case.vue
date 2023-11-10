<template>
  <main>
    <section class="container">
      <section class="hero bg-[#D3DEE5] px-[1.5rem] pb-8">
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
      </section>
      <section class="section1 h-[100vh] relative text-[#0D283F] bg-[#D3DEE5]">
        <img class="img" src="../assets/ps.jpg" alt="" />
        <div class="desc1 absolute top-80 pt-16 px-[1.5rem] md:top-[34rem]">
          <h2 class="text-[#FF4A31] text-[1rem] font-[800] uppercase">
            key challenge to solve
          </h2>
          <p class="text-[1.375rem] font-[800] pt-4">
            To highlight the main challenges of the project (initial problems or
            problems encountered during the process), focusing on the main ones,
            so that it is clear to everyone what we had to solve.
          </p>
        </div>
        <div
          class="desc2 absolute top-[39rem] pt-16 px-[1.5rem] md:top-[52rem]"
        >
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
        <div
          class="desc3 absolute top-[57rem] pt-16 px-[1.5rem] md:top-[72rem]"
        >
          <h2 class="text-[#FF4A31] text-[1rem] font-[800] uppercase">
            result
          </h2>
          <p class="text-[1.375rem] font-[800] pt-4">
            We have developed a mobile competence center that supports agile
            delivery and decreases time to market, resulting in a fast and
            easily scalable mobile application.
          </p>
          <div class="relative grid justify-center items-center pt-16">
            <div
              class="box1 absolute top-12 left-20 text-[#001826] p-[3rem] bg-white rounded-[2rem] w-[19rem] flex items-center justify-center flex-col"
            >
              <p class="text-[3.5rem] font-[500] pb-[1.5rem]">4,4</p>
              <p class="text-[1.125rem] font-[600]">Based on 23 000</p>
              <p class="text-[1.125rem] font-[600]">Appstore review</p>
            </div>
            <div
              class="box2 absolute top-16 left-20 text-[#001826] p-[3rem] bg-white rounded-[2rem] w-[19rem] flex items-center justify-center flex-col"
            >
              <p class="text-[3.5rem] font-[500] pb-[1.5rem]">4,4</p>
              <p class="text-[1.125rem] font-[600]">Based on 23 000</p>
              <p class="text-[1.125rem] font-[600]">Appstore review</p>
            </div>
            <div
              class="box3 absolute top-20 left-20 text-[#001826] p-[3rem] bg-white rounded-[2rem] w-[19rem] flex items-center justify-center flex-col"
            >
              <p class="text-[3.5rem] font-[500] pb-[1.5rem]">4,4</p>
              <p class="text-[1.125rem] font-[600]">Based on 23 000</p>
              <p class="text-[1.125rem] font-[600]">Appstore review</p>
            </div>
          </div>
        </div>
      </section>
      <section>
        <p>
          “It was fun to break from our routine of building MVPs with
          early-stage startups to blend into a team of executives. Spoiler: we
          did just as good.”
        </p>
      </section>
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
    let tl = gsap.timeline({
      scrollTrigger: {
        trigger: '.container',
        pin: '.container',
        pinSpacer: false,
        //pinSpacing: false,
        markers: true,
        scrub: 1,
      },
    })
    tl.set(['.desc1', '.desc2', '.desc3', '.box1', '.box2', '.box3'], {
      opacity: 0,
      y: 150,
    })
      .to('.hero', {
        opacity: 0,
      })
      .to(
        '.section1',
        {
          y: -600,
        },
        '<'
      )
      .to(
        '.desc1',
        {
          opacity: 4,
          y: 0,
        },
        '<'
      )
      .to('.desc1', {
        opacity: 0,
      })
      .to('.desc2', {
        opacity: 4,
        y: -300,
      })
      .to('.desc2', {
        opacity: 0,
      })
      .to('.desc3', {
        opacity: 4,
        y: -600,
      })
      .to('.img', {
        y: -200,
        opacity: 0,
      })
      .to(
        '.desc3',
        {
          y: -800,
        },
        '<'
      )
      .to('.box1', {
        y: 0,
        opacity: 4,
      })
      .to('.box1', {
        scale: 0.6,
        opacity: 0.6,
      })
      .to(
        '.box2',
        {
          y: 25,
          opacity: 4,
        },
        '<'
      )
      .to('.box2', {
        scale: 0.8,
        opacity: 0.8,
      })
      .to(
        '.box3',
        {
          y: 50,
          opacity: 4,
        },
        '<'
      )
  },
}
</script>
<style lang=""></style>
