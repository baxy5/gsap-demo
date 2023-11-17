<template>
  <main class="overflow-hidden">
    <div
      id="container"
      class="relative bg-white h-[100vh] w-full flex justify-center items-center"
    >
      <p
        id="text1"
        class="absolute top-[40%] left-[20%] text-white text-[2rem] lg:text-[4rem] z-50"
      >
        We love to wow
      </p>
      <p
        id="text2"
        class="absolute top-[40%] left-[20%] text-white text-[2rem] lg:text-[4rem] z-50"
      >
        We love to wow2
      </p>
      <p class="absolute text-black text-[6rem] appic z-50 mt-96">Appic</p>
      <svg
        class="svg h-full w-full z-40"
        width="1794"
        height="1219"
        viewBox="0 0 1794 1219"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <defs>
          <linearGradient id="gradient" x1="0%" y1="0%" x2="100%" y2="0%">
            <stop offset="0%" style="stop-color: rgba(53, 48, 139, 1)" />
            <stop offset="35%" style="stop-color: rgba(96, 96, 213, 1)" />
            <stop offset="100%" style="stop-color: rgba(0, 212, 255, 1)" />
          </linearGradient>
        </defs>
        <path
          id="path"
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M1203.94 43.3272C1203.94 19.3983 1184.54 0 1160.61 0H705.23C681.587 0 658.97 9.66102 642.623 26.7432L16.0239 681.537C5.73962 692.284 -0.00048825 706.586 3.11491e-08 721.461L0.0140398 1175.02C0.0147805 1198.95 19.4128 1218.35 43.3413 1218.35H498.734C522.366 1218.35 544.972 1208.69 561.311 1191.62L1033.94 697.711C1060.95 669.489 1108.58 688.606 1108.58 727.668L1108.57 1005.66C1108.57 1027.57 1116.87 1048.67 1131.81 1064.71L1257.56 1199.66C1268.49 1211.38 1283.79 1218.04 1299.81 1218.04H1749.74C1773.66 1218.04 1793.06 1198.64 1793.06 1174.71L1793.08 726.39C1793.08 708.127 1786.15 690.542 1773.7 677.181L1648.36 542.676C1634.7 528.018 1615.57 519.694 1595.53 519.694H1247.27C1223.34 519.694 1203.94 500.296 1203.94 476.367V43.3272Z"
          fill="#001323"
        />
      </svg>
    </div>
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
        trigger: '.svg',
        scrub: 1,
        pin: '#container',
        pinSpacer: false,
        start: 'center center',
      },
    })

    let mm = gsap.matchMedia()

    mm.add('(min-width: 1024px)', () => {
      tl.set(['#text1', '#text2'], {
        opacity: 0,
        y: 120,
      })
        .set('.appic', {
          opacity: 0,
        })
        .set('.svg', {
          scale: 8,
        })
        .to('.svg', {
          scale: 2.5,
        })
        .to('#text1', {
          opacity: 4,
          y: 0,
        })
        .to('#text1', {
          opacity: 0,
          y: -120,
        })
        .to('.svg', {
          scale: 1.5,
        })
        .to('#text2', {
          opacity: 4,
          y: 0,
        })
        .to('#text2', {
          opacity: 0,
          y: -120,
        })
        .to('.svg', {
          scale: 0.3,
        })
        .to(
          '#path',
          {
            fill: 'url(#gradient)',
          },
          '<'
        )
        .to('.appic', {
          opacity: 4,
          display: 'block',
        })
    })

    mm.add('(max-width: 1023px)', () => {
      tl.set(['#text1', '#text2'], {
        opacity: 0,
        y: 120,
      })
        .set('.appic', {
          opacity: 0,
        })
        .set('.svg', {
          scale: 8,
        })
        .to('.svg', {
          scale: 2.5,
        })
        .to('#text1', {
          opacity: 4,
          y: 0,
        })
        .to('#text1', {
          opacity: 0,
          y: -120,
        })
        .to('.svg', {
          scale: 1.5,
        })
        .to('#text2', {
          opacity: 4,
          y: 0,
        })
        .to('#text2', {
          opacity: 0,
          y: -120,
        })
        .to('.svg', {
          scale: 0.4,
        })
        .to(
          '#path',
          {
            fill: 'url(#gradient)',
          },
          '<'
        )
        .to('.appic', {
          opacity: 4,
          display: 'block',
        })
    })
  },
}
</script>
