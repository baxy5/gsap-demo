<template>
  <main class="overflow-hidden">
    <div
      id="wow-container"
      class="relative bg-[#001323] h-[100vh] w-full flex justify-center items-center"
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
      <p
        class="appic absolute text-black text-[6rem] z-50 mt-96 font-extrabold"
      >
        appic
      </p>
      <svg
        class="svg h-full w-full z-40"
        width="32768"
        height="8739"
        viewBox="0 0 32768 8739"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M32768 0H0V8738.13H32768V0ZM16770.4 3481.6H16106.5C16072.1 3481.6 16039.1 3495.69 16015.3 3520.59L15101.8 4475.2C15086.8 4490.87 15078.4 4511.72 15078.4 4533.4L15078.4 5194.64C15078.4 5229.52 15106.7 5257.8 15141.6 5257.8H15805.5C15839.9 5257.8 15872.9 5243.72 15896.7 5218.83L16585.8 4498.77C16625.1 4457.63 16694.6 4485.5 16694.6 4542.44L16694.6 4947.73C16694.6 4979.68 16706.7 5010.44 16728.5 5033.81L16911.8 5230.56C16927.7 5247.64 16950 5257.35 16973.4 5257.35H17629.3C17664.2 5257.35 17692.5 5229.07 17692.5 5194.19L17692.5 4540.59C17692.5 4513.96 17682.4 4488.33 17664.2 4468.85L17481.5 4272.76C17461.6 4251.39 17433.7 4239.25 17404.5 4239.25H16896.8C16861.9 4239.25 16833.6 4210.97 16833.6 4176.09V3544.77C16833.6 3509.88 16805.3 3481.6 16770.4 3481.6Z"
          fill="white"
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
          end: '+=10500',
          fastScrollEnd: true,
        },
      })

      // "We love to wow" - animation
      let textAnimation = gsap.timeline({
        scrollTrigger: {
          trigger: '#text1',
          start: 'top top',
          end: '+=4000px',
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
          scale: 1,
          duration: 1,
        })
        .to('#text1', {
          scale: 0,
          opacity: 0,
        })
        .from(
          '#text2',
          {
            scale: 4,
            opacity: 0,
          },
          '-=0.3'
        )
        .to('#text2', {
          scale: 1,
          duration: 1,
        })
        .to('#text2', {
          scale: 0,
          opacity: 0,
        })

      appicLogoAnimation
        .set('.appic', {
          opacity: 0,
          y: 40,
        })
        .set('.svg', {
          scale: 90,
        })
        .to('.svg', {
          scale: 12.5,
        })
        .to('#wow-container', {
          background:
            'conic-gradient(from -90deg at 50.84% 49.95%, #5BFFB0 95.75302720069885deg, #2279C9 179.20027256011963deg, #6CCBF4 284.6290683746338deg), #D9D9D9',
        })
        .to(
          '.svg',
          {
            scale: 3,
          },
          '<'
        )
        /* .to('.svg', {
          scale: 3,
          onUpdate: () => {
            if (gsap.getProperty('.svg', 'scale') <= 12.5) {
              gsap.to(
                '#wow-container',
                {
                  background:
                    'conic-gradient(from -90deg at 50.84% 49.95%, #5BFFB0 95.75302720069885deg, #2279C9 179.20027256011963deg, #6CCBF4 284.6290683746338deg), #D9D9D9',
                },
                '<'
              )
            } else {
              gsap.to(
                '#wow-container',
                {
                  background: '#001323',
                },
                '<'
              )
            }
          },
        }) */
        .to('.appic', {
          opacity: 4,
          y: 0,
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
