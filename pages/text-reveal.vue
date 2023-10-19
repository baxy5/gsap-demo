<template>
  <main class="wrapp bg-[#0a0a0a]">
    <div class="header">
      <h1 class="title">
        <span class="title_paralax">
          <span class="char">B</span>
          <span class="char">a</span>
          <span class="char"> l </span>
          <span class="char"> d </span>
          <span class="char"> u </span>
          <span class="char"> r </span>
          <span class="char">'</span>
          <span class="char">s</span>
        </span>
        <span> </span>
        <span class="stroke">
          <span class="char">G</span>
          <span class="char">a</span>
          <span class="char">t</span>
          <span class="char">e</span>
        </span>
      </h1>
      <div class="header__img">
        <img src="../assets/b2.jpg" alt="1" />
      </div>
    </div>
    <div class="pt-40 px-32 text-white flex gap-[4rem]">
      <div class="testimage">
        <img src="../assets/ps.jpg" alt="1" />
      </div>
      <div class="pt-56 w-[48rem]">
        <p class="parag text-lg font-bold">
          To highlight the main challenges of the project (initial problems or
          problems encountered during the process), focusing on the main ones,
          so that it is clear to everyone what we had to solve.
        </p>
      </div>
    </div>
    <div class="h-[200vh]"></div>
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
    // header betöltésnél
    const tl = gsap.timeline()
    tl.from('.title .char', {
      opacity: 0,
      yPercent: 130,
      stagger: 0.06,
      ease: 'back.out',
      duration: 1,
    })

    tl.to(
      '.header__img',
      {
        clipPath: 'polygon(0% 0%, 100% 0%, 100% 100%, 0% 100%)',
        scale: 1,
        ease: 'expo.out',
        duration: 5,
      },
      '-=1'
    )

    // header görgetésnél
    gsap.to('.title_paralax', {
      scrollTrigger: {
        trigger: '.header',
        start: 'top top',
        scrub: 1.9,
      },
      yPercent: -150,
    })

    gsap.to('.header__img', {
      scrollTrigger: {
        trigger: '.header',
        start: 'top top',
        scrub: 1.9,
      },
      xPercent: -70,
    })
    gsap.to('.header__img img', {
      scrollTrigger: {
        trigger: '.header',
        start: 'top top',
        scrub: 1.9,
      },
      scale: 2,
    })

    // section 2
    gsap.set('.parag', {
      y: 100,
      x: -300,
      opacity: 0,
    })
    gsap.to('.parag', {
      scrollTrigger: {
        trigger: '.parag',
        scrub: true,
      },
      y: -100,
      opacity: 2,
    })

    gsap.set('.testimage', {
      clipPath: 'polygon(0 0, 100% 0, 100% 100%, 0 100%)',
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

<style>
.wrapp {
  width: 100%;
  height: auto;
  overflow: hidden;
  z-index: 1;
}

.char {
  display: inline-block;
}

.header {
  position: relative;
  display: flex;
  padding: 0 70px;

  align-items: center;
  width: 100%;
  height: 100vh;
}

.title {
  position: relative;
  margin: 0;
  font-size: 85px;
  text-align: center;
  padding-left: 350px;
  color: #fff;
  text-transform: uppercase;
  mix-blend-mode: difference;
  z-index: 2;
}

.title_paralax {
  display: inline-block;
  will-change: transform;
}

.title .stroke {
  display: inline-block;
  color: transparent;
  -webkit-text-stroke: 1px #fff;
}

.header__img {
  position: absolute;
  width: 45%;
  height: 100%;
  top: 0;
  right: 100px;
  clip-path: polygon(0% 0%, 0% 0%, 0% 100%, 0% 100%);
  overflow: hidden;
}

.header__img img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
