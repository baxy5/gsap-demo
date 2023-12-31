<template>
  <main id="main-container" class="bg-[#D3DEE5] px-[12.13rem] text-[#0D283F]">
    <div class="hero-text">
      <div class="flex justify-between px-52 pt-52">
        <div id="intro" class="w-[500px] text-[#0D283F]">
          <h1 class="text-[3.5rem] font-bold text-orange-500">Project title</h1>
          <p class="text-[1.75rem] font-bold">
            Short text about the project. What it is, what impact it has had.
            Who we worked with, maybe a few words about the partner. In 3-5
            lines. Highlight the main point & make it interesting.
          </p>
        </div>
        <div id="tags" class="translate-y-24 text-[#0D283F]">
          <p class="font-bold text-[1rem] uppercase pb-4">Services</p>
          <ul class="grid gap-4">
            <li class="bg-white rounded-full p-2">Product Design</li>
            <li class="bg-white rounded-full p-2">Design System</li>
            <li class="bg-white rounded-full p-2">Webdesign</li>
            <li class="bg-white rounded-full p-2">App Design</li>
          </ul>
          <p class="font-bold text-[1rem] uppercase pb-4 pt-4">Industries</p>
          <ul class="grid gap-4">
            <li class="bg-white rounded-full p-2">Product Design</li>
            <li class="bg-white rounded-full p-2">Design System</li>
          </ul>
          <p class="font-bold text-[1rem] uppercase pb-4 pt-4">Technologies</p>
          <ul class="grid gap-4">
            <li class="bg-white rounded-full p-2">Product Design</li>
            <li class="bg-white rounded-full p-2">Design System</li>
          </ul>
        </div>
      </div>
    </div>
    <div id="image-container">
      <div class="pt-8 text-black overflow-hidden flex">
        <div class="anim-img w-[70%] object-cover relative">
          <img src="../assets/ps.jpg" alt="1" />
        </div>
        <div class="absolute h-full w-full">
          <div class="absolute right-[10%] top-[35%] w-[500px]">
            <div id="parag1" class="absolute text-[1.75rem] font-bold">
              <h2 class="uppercase text-[#FF4A31] text-[1rem] pb-8">
                Key challenge to solve
              </h2>
              <p class="text-[#0D283F]">
                To highlight the main challenges of the project (initial
                problems or problems encountered during the process), focusing
                on the main ones, so that it is clear to everyone what we had to
                solve.
              </p>
            </div>
            <div id="parag2" class="absolute text-[1.75rem] font-bold">
              <h2 class="uppercase text-[#FF4A31] text-[1rem] pb-8">
                Our process in bullet points
              </h2>
              <ul class="grid gap-8 text-[#0D283F]">
                <li class="flex gap-4">
                  <img src="../assets/case-search.svg" alt="asd" />
                  <p>List item</p>
                </li>
                <li class="flex gap-4">
                  <img src="../assets/case-search.svg" alt="asd" />
                  <p>List item</p>
                </li>
                <li class="flex gap-4">
                  <img src="../assets/case-search.svg" alt="asd" />
                  <p>List item</p>
                </li>
                <li class="flex gap-4">
                  <img src="../assets/case-search.svg" alt="asd" />
                  <p>List item</p>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="absolute w-full top-[25%] flex justify-between">
          <div id="box-text" class="w-[34rem]">
            <h2 class="text-[#FF4A31] uppercase text-[1rem] font-extrabold">
              Result
            </h2>
            <p class="text-[#0D283F] text-[1.75rem] font-bold">
              We have developed a mobile competence center that supports agile
              delivery and decreases time to market, resulting in a fast and
              easily scalable mobile application.
            </p>
          </div>
          <div
            id="box1"
            class="absolute top-[90%] right-[25%] bg-white p-16 rounded-[2rem] text-center"
          >
            <div>
              <h2 class="text-[3.75rem] font-medium">XX</h2>
              <p class="text-[1.125rem] font-semibold">
                Based on 23 000 <br />
                Appstore review
              </p>
            </div>
          </div>
          <div
            id="box2"
            class="absolute top-[90%] right-[25%] bg-white p-16 rounded-[2rem] text-center"
          >
            <div>
              <h2 class="text-[3.75rem] font-medium">20%</h2>
              <p class="text-[1.125rem] font-semibold">
                Based on 23 000 <br />
                Appstore review
              </p>
            </div>
          </div>
          <div
            id="box3"
            class="absolute top-[90%] right-[25%] bg-white p-16 rounded-[2rem] text-center"
          >
            <div>
              <h2 class="text-[3.75rem] font-medium">4,4</h2>
              <p class="text-[1.125rem] font-semibold">
                Based on 23 000 <br />
                Appstore review
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="h-[100vh]">next section</div>
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
    // Hero Animation
    let heroAnim = gsap.timeline({
      scrollTrigger: {
        trigger: '.hero-text',
        start: 'top top',
        end: '+=1000',
        scrub: 1,
      },
    })

    heroAnim
      .set('.anim-img', {
        clipPath: 'polygon(0 0, 100% 0, 100% 100%, 0 100%)',
        transform: 'scale(1)',
      })
      .to(['#intro', '#tags'], {
        y: '-100%',
        opacity: 0,
      })
      .to(
        '.anim-img',
        {
          clipPath: 'polygon(0 0, 60% 0, 60% 100%, 0 100%)',
        },
        '<'
      )

    // Image Animation
    let imageOnTextAnim = gsap.timeline({
      scrollTrigger: {
        trigger: '#image-container',
        start: 'top top+=60',
        end: '+=7500',
        scrub: 1,
        pin: '#image-container',
      },
    })

    imageOnTextAnim
      .set(['#parag1', '#parag2'], {
        opacity: 0,
        y: 250,
      })
      .set(['#box-text', '#box1'], {
        opacity: 0,
        y: 250,
      })
      .set(['#box2', '#box3'], {
        opacity: 0,
        y: 250,
      })
      .to('#parag1', {
        opacity: 4,
        y: 0,
      })
      .to('#parag1', {
        opacity: 0,
        y: -250,
      })
      .to('.anim-img', {
        transform: 'scale(1.5) translate(-450px, 0%)',
        clipPath: 'polygon(0 0, 100% 0, 100% 100%, 0 100%)',
      })
      .to(
        '#parag2',
        {
          opacity: 4,
          y: 0,
        },
        '<'
      )
      .to('#parag2', {
        opacity: 0,
        y: -25,
        x: 25,
      })
      .to(
        '.anim-img',
        {
          transform: 'scale(1) translate(20%, 0%)',
          clipPath: 'polygon(0 0, 100% 0, 100% 100%, 0 100%)',
          duration: 1,
        },
        '<'
      )
      .to(
        '#main-container',
        {
          backgroundColor: '#0D283F',
        },
        '<'
      )
      .to('#main-container', {
        backgroundColor: '#D3DEE5',
      })
      .to(
        '.anim-img',
        {
          opacity: 0,
          y: '-100%',
        },
        '<'
      )
      .to(
        ['#box-text', '#box1'],
        {
          opacity: 4,
          y: 0,
        },
        '<'
      )
      .to('#box1', {
        opacity: 0.6,
        scale: 0.6,
        color: 'transparent',
      })
      .to(
        '#box2',
        {
          opacity: 4,
          y: 60,
        },
        '<'
      )
      .to('#box2', {
        opacity: 0.8,
        scale: 0.8,
        color: 'transparent',
      })
      .to(
        '#box3',
        {
          opacity: 4,
          y: 120,
        },
        '<'
      )
  },
}
</script>
