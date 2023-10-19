<template>
  <main class="overflow-hidden">
    <section
      class="w-100 h-[100vh] bg-[#001323] flex justify-center items-center"
    >
      <div ref="title">
        <img src="../assets/appic-logo.png" alt="a" height="150" width="150" />
        <h2 class="text-white">Only GSAP (atropos vue was removed)</h2>
      </div>
    </section>

    <section
      class="voda pt-48 w-full h-[100vh] p-[3.81rem] flex gap-[4.71rem] bg-[#001323] text-white"
    >
      <div class="vod w-[30rem]">
        <h1 class="text-[3.5rem] font-bold">MOL</h1>
        <p class="text-[2rem]">
          Short text about the project. What it is, what impact it has had. Who
          we worked with, maybe a few words about the partner. In 3-5 lines.
          Highlight the main point & make it interesting.
        </p>
      </div>
      <div class="vod flex justify-center items-center">
        <img src="../assets/voda-mobile.png" alt="v" />
        <img src="../assets/voda-mobile.png" alt="v" />
        <img src="../assets/voda-mobile.png" alt="v" />
      </div>
    </section>
  </main>
</template>

<script>
// GSAP
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

if (typeof window !== 'undefined') {
  gsap.registerPlugin(ScrollTrigger)
}

export default {
  mounted() {
    // title fade out and fixed
    const title = this.$refs.title
    const section = title.parentElement

    gsap.set(title, { opacity: 4 })
    gsap.to(title, {
      opacity: 0,
      position: 'fixed',
      scrollTrigger: {
        trigger: section,
        start: 'top center',
        end: 'bottom center',
        scrub: 1,
      },
    })

    // create timeline for first section
    const tl1 = gsap.timeline({
      scrollTrigger: {
        trigger: '.voda',
        start: 'bottom bottom',
        end: () => innerHeight * 7,
        scrub: 2,
        pin: '.voda',
        anticipatePin: 1,
      },
    })

    tl1
      .set('.vod', { autoAlpha: 0 })
      .to('.vod', { duration: 0.1, autoAlpha: 1 }, 0.001)
      .from('.vod', {
        scale: 2.3333,
        ease: 'none',
      })
      .to('.vod', {
        scale: 1,
        duration: 0.3,
        ease: 'none',
      })
      .to('.vod', {
        scale: 0.3,
        opacity: 0,
        duration: 1,
        ease: 'none',
      })
      .to('.vod', {
        scale: -3.33,
        ease: 'none',
      })
  },
}
</script>
