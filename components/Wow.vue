<template>
  <main class="overflow-hidden">
    <div
      id="wow-container"
      class="relative bg-white h-[100vh] w-full flex justify-center items-center"
    >
      <p
        id="text1"
        class="absolute flex justify-center items-center text-white text-[3.5rem] lg:text-[7rem] z-50"
      >
        We love to wow
      </p>
      <p
        id="text2"
        class="absolute top-[40%] left-[20%] text-white text-[3.5rem] lg:text-[4rem] z-50"
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
          <radialGradient id="gradient" cx="68%" cy="35%" r="100%">
            <stop offset="27%" style="stop-color: #5bffb0" />
            <stop offset="50%" style="stop-color: #2279c9" />
            <stop offset="79%" style="stop-color: #6ccbf4" />
          </radialGradient>
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
    let mm = gsap.matchMedia()

    mm.add('(min-width: 1024px)', () => {
      // Appic Logo animáció
      let appicLogoAnimation = gsap.timeline({
        scrollTrigger: {
          trigger: '#wow-container',
          scrub: 1,
          pin: '#wow-container',
          pinSpacer: false, // ez a kettö amugy fölösleges szerintem ide mert semmit nem csinálnak kb
          pinSpacig: false, // ez is megrohadhat
          start: 'top top',
          end: '+=7400',
          fastScrollEnd: true,
        },
      })

      // "We love to wow" - animation
      let textAnimation = gsap.timeline({
        scrollTrigger: {
          trigger: '#text1',
          start: 'top top',
          end: '+=2500px',
          scrub: 1,
          fastScrollEnd: true,
        },
      })

      textAnimation
        .from('#text1', {
          scale: 4,
          opacity: 0,
        })
        .to('#text1', {
          scale: 0,
          opacity: 0,
        })
        .from('#text2', {
          scale: 4,
          opacity: 0,
        })
        .to('#text2', {
          scale: 0,
          opacity: 0,
        })

      appicLogoAnimation
        .set('.appic', {
          opacity: 0,
        })
        .set('.svg', {
          scale: 8,
        })
        .to('.svg', {
          scale: 0.3,
          onUpdate: () => {
            if (gsap.getProperty('.svg', 'scale') <= 1.8) {
              gsap.to(
                '#path',
                {
                  fill: 'url(#gradient)',
                },
                '<'
              )
            } else {
              gsap.to(
                '#path',
                {
                  fill: '#001323',
                },
                '<'
              )
            }
          },
        })
        .to('.appic', {
          opacity: 4,
          display: 'block',
        })
    })

    mm.add('(max-width: 1023px)', () => {
      // Appic Logo animáció
      let appicLogoAnimation = gsap.timeline({
        scrollTrigger: {
          trigger: '#wow-container',
          scrub: 1,
          pin: '#wow-container',
          pinSpacer: false, // ez a kettö amugy fölösleges szerintem ide mert semmit nem csinálnak kb
          pinSpacig: false, // ez is megrohadhat
          start: 'top top',
          end: '+=4400',
        },
      })

      // "We love to wow" - animation
      let textAnimation = gsap.timeline({
        scrollTrigger: {
          trigger: '#text1',
          start: 'top top',
          end: '+=1200px',
          scrub: 1,
        },
      })

      textAnimation
        .from('#text1', {
          scale: 4,
          opacity: 0,
        })
        .to('#text1', {
          scale: 0,
          opacity: 0,
        })
        .from('#text2', {
          scale: 4,
          opacity: 0,
        })
        .to('#text2', {
          scale: 0,
          opacity: 0,
        })

      appicLogoAnimation
        .set('.appic', {
          opacity: 0,
        })
        .set('.svg', {
          scale: 8,
        })
        .to('.svg', {
          scale: 0.3,
          onUpdate: () => {
            if (gsap.getProperty('.svg', 'scale') <= 1.8) {
              gsap.to(
                '#path',
                {
                  fill: 'url(#gradient)',
                },
                '<'
              )
            } else {
              gsap.to(
                '#path',
                {
                  fill: '#001323',
                },
                '<'
              )
            }
          },
        })
        .to('.appic', {
          opacity: 4,
          display: 'block',
        })
    })
  },
}
</script>
