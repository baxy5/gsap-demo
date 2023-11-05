<template>
  <main class="overflow-hidden">
    <section
      class="w-full h-[100vh] text-white bg-[#0a0a0a] flex flex-col justify-center items-center"
    >
      <div class="hero flex flex-col justify-center items-center">
        <h1 class="text-7xl font-bold pb-12">GSAP Animations demo</h1>
        <div class="grid gap-5">
          <p class="text-xl">"/" : főoldal pár egyszerübb bemutato animácio</p>
          <p class="text-xl">
            "/boxes" : properties, scrub, részletesebben az animáciok
          </p>
          <p class="text-xl">
            "/scroll-to-view" : appices animácio probálkozás
          </p>
          <p class="text-xl">
            "/text-reveal" : lehetosegek + 1 appices animácio
          </p>
          <p class="text-xl">
            "/appic-main" : appic főoldal animáció
          </p>
          <p class="text-xl">
            "/case-study" : appic case study animáció
          </p>
        </div>
      </div>
    </section>
    <div class="h-[100vh] w-full">
      <h1 class="text-5xl font-bold text-center">
        Néhány egyszerübb animácio:
      </h1>
      <div
        ref="main"
        class="w-full h-[100vh] flex flex-col gap-5 justify-center items-center"
      >
        <h2 class="text-3xl font-bold">
          Scrub animation with a 3 second delay
        </h2>
        <div class="box bg-red-500 border-2 border-black p-5 rounded-sm">
          Box1
        </div>
        <div class="box bg-red-500 border-2 border-black p-5 rounded-sm">
          Box2
        </div>
        <div class="box bg-red-500 border-2 border-black p-5 rounded-sm">
          Box3
        </div>

        <h2 class="pt-32 text-3xl font-bold">Scrub progress bar animation</h2>
        <div>
          <p class="line line-1"></p>
          <p>
            This line's animation will begin when it enters the viewport and
            finish when its top edge hits the top of the viewport, staying
            perfectly in sync with the scrollbar because it has
            <code>scrub:&nbsp;true</code>
          </p>
        </div>
      </div>
    </div>
    <div class="w-full h-[100vh] bg-[#0a0a0a] text-white orange px-2">
      <h2 class="pt-32 text-3xl font-bold">
        Scrub progress bar pinned animation
      </h2>
      <section id="three" class="panel">
        <p>
          <span class="line line-2"></span>This orange panel gets pinned when
          its top edge hits the top of the viewport, then the line's animation
          is linked with the scroll position until it has traveled 100% of the
          viewport's height (<code>end: "+=100%"</code>), then the orange panel
          is unpinned and normal scrolling resumes. Padding is added
          automatically to push the rest of the content down so that it catches
          up with the scroll when it unpins. You can set
          <code>pinSpacing: false</code> to prevent that if you prefer.
        </p>
      </section>
    </div>

    <div
      class="w-full bg-[#0a0a0a] h-[100vh] flex flex-col justify-center items-center"
    >
      <h1>Placeholder</h1>
    </div>
  </main>
</template>

<script>
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

if (typeof window !== 'undefined') {
  gsap.registerPlugin(ScrollTrigger)
}

export default {
  name: 'gsap-demo',
  mounted() {
    this.ctx = gsap.context((self) => {
      const boxes = self.selector('.box')
      boxes.forEach((box) => {
        gsap.to(box, {
          x: 150,
          scrollTrigger: {
            trigger: box,
            start: 'bottom bottom', // when the bottom of the trigger hits the bottom of the viewport
            end: 'top 50%', // end after scrolling 50% from the top beyond the start
            scrub: 3, // smooth scrubbing, takes 3 second to "catch up" to the scrollbar
          },
        })
      })
    }, this.$refs.main)

    gsap.from('.line-1', {
      scrollTrigger: {
        trigger: '.line-1',
        scrub: true,
        start: 'top bottom',
        end: 'top top',
      },
      scaleX: 0,
      transformOrigin: 'left center',
      ease: 'none',
    })

    gsap.from('.line-2', {
      scrollTrigger: {
        trigger: '.orange',
        scrub: true,
        pin: true,
        start: 'top top',
        end: '+=100%',
      },
      scaleX: 0,
      transformOrigin: 'left center',
      ease: 'none',
    })
  },
  beforeDestroy() {
    this.ctx.revert()
  },
}
</script>

<style>
.line {
  width: 100%;
  max-width: 100%;
  height: 8px;
  margin: 0 0 10px 0;
  position: relative;
  display: inline-block;
  background-color: rgb(255, 1, 1);
}
</style>
