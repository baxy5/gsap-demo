<template>
  <main class="bg-[#001323] h-full">
    <section class="h-[50vh] p-32">
      <h1 class="text-[2.5rem] text-white">Properties: (lényegesebb)</h1>
      <div class="text-white">
        <p>
          `markers` -> Amit a szélén látsz, mutatja mikor kezd és végez a scrub
          animáció (fejlesztéshez)
        </p>
        <p>
          `scrub` -> Alapvetően az animácó lefut ahogy betölt az oldal (box1),
          de ha ez 'true' és a scrollTrigger segitségével számitásba veszi a
          görgetést is. (box2). Ezek mellett ez nem csak 'true' lehet. Például
          ha egy 2-es értéket adunk neki akkor 2 masodpercel késik az animáció
          ez által egy smoothabb hatást kelt. (box3)
        </p>
        <p>
          `timeline` -> Ennek a segitségével complexebb animációkat is létre
          lehet hozni.
        </p>
        <p>
          `ease` -> Az animáció idözitése, legegyszerübb ha ezen a kiraly
          oldalon megnezed mert itt vizulizálva van mindenegyes ease:
          https://gsap.com/docs/v3/Eases
        </p>
        <p>
          `pin` -> Erről példák: <br /><span>- "/" oldalon</span> <br /><span
            >- "/scroll-to-view" oldalon</span
          >
        </p>
        <p>
          Ez pár főbb prop, hogy demonstráljam hogy kb mire képes, de mindent is
          lehet mindennel füszerezni.
        </p>
      </div>
    </section>
    <section class="h-[100vh] pt-32 pl-32">
      <h1 class="box text-white p-5 border-2 border-white w-20">box1</h1>
    </section>
    <section class="h-[100vh] pt-32 pl-32">
      <h1 class="box2 text-white p-5 border-2 border-white w-20">box2</h1>
    </section>
    <section class="h-[100vh] pt-32 pl-32">
      <h1 class="box3 text-white p-5 border-2 border-white w-20">box3</h1>
    </section>
    <section class="h-[100vh] pt-32 pl-32">
      <h1 class="text-white p-5 border-2 border-white w-20">box4</h1>
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
    // box1
    gsap.to('.box', {
      x: 400,
      rotate: 360,
      duration: 5,
    })

    // box2
    let tl = gsap.timeline({
      scrollTrigger: {
        trigger: '.box2',
        start: 'top center',
        markers: true,
        scrub: true,
      },
    })

    tl.to('.box2', {
      x: 900,
      rotate: 360,
    })

    //box3
    gsap.to('.box3', {
      scrollTrigger: {
        trigger: '.box3',
        start: 'top center',
        markers: true,
        scrub: 2,
      },
      x: 900,
      rotate: 360,
    })
  },
}
</script>
