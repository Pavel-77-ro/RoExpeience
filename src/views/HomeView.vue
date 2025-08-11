<script setup>
import NavBar from '../components/NavBar.vue'
import FooterSection from '../components/FooterSection.vue'
import { useRouter } from 'vue-router'

const router = useRouter()

function toMap() {
  router.push({ name: 'contact' })
}

function toAbout() {
  router.push({ name: 'about' })
}
</script>

<template>
  <NavBar />
  <!-- Hero -->
  <section class="relative">
    <div class="container flex flex-col-reverse lg:flex-row items-center gap-12 mt-20 lg:mt-32 xl:px-12">
      <!-- Content -->
      <div class="flex flex-1 flex-col items-center lg:items-start">
        <h2
          class="text-bookmark-blue text-3xl md:text-4 lg:text-5xl text-center font-semibold lg:text-left mb-6"
        >
          RoExperience
        </h2>
        <p class="text-bookmark-grey text-lg text-center lg:text-left mb-6">
          Actvitati recreative si sportive potrivite pentru oricine. Alege sa iti petreci timpul liber intr-un mod placut si sanatos, alaturi de cei dragi.
          .
        </p>
        <div class="flex justify-center flex-wrap gap-6">
          <button
            type="button"
            class="btn btn-purple hover:bg-gray-600 transition font-Lucky text-xl md:text-2xl tracking-wider"
            @click="toMap()"
          >
            Visit Us
          </button>
        </div>
      </div>
      <!-- Image -->
      <div class="flex justify-center flex-1 mb-10 md:mb-16 lg:mb-0 z-10">
        <img
          class="w-5/6 h-5/6 sm:w-3/4 sm:h-3/4 md:w-full md:h-full"
          src="../assets/illustrations/soleta_main.png"
          alt=""
        />
      </div>
    </div>
  </section>

  <!-- Features -->
<section class="bg-bookmark-white py-20 mt-28 lg:mt-60 pb-64 relative">
  <!-- Heading -->
  <div class="sm:w-3/4 lg:w-5/12 mx-auto px-2">
    <h1 class="text-3xl text-center text-bookmark-blue">Ce ne diferențiază</h1>
    <p class="text-center text-bookmark-grey mt-4">
      La RoExperience pui pauză de la agitație și petreci timp de calitate alături de ai tăi.
      Am gândit locul simplu, curat și prietenos, cu spații care se adaptează grupului și
      cu un ritm în care chiar te relaxezi.
    </p>
  </div>

  <!-- Feature #1 -->
  <div class="relative mt-24 lg:mt-32">
    <div class="container flex flex-col lg:flex-row items-center justify-center gap-x-24">
      <!-- Image -->
      <div class="flex flex-1 justify-center z-10 mb-10 lg:mb-0">
        <img class="w-3/4 h-3/4 md:w-full md:h-full rounded-4xl" src="../assets/illustrations/activ_centru.png" alt="Activități la centru" />
      </div>
      <!-- Content -->
      <div class="flex flex-1 flex-col items-center lg:items-start">
        <h1 class="text-3xl text-bookmark-blue">Totul pregătit pentru o zi reușită</h1>
        <p class="text-bookmark-grey my-4 text-center lg:text-left sm:w-3/4 lg:w-full">
          Fără bătăi de cap cu „logistica”. Avem pavilion acoperit, zonă verde pentru jocuri,
          tabla interactiva pentru seri de film, vatră de foc, hamace și materiale pentru ateliere.
          Treci ușor între interior și curte, păstrezi atmosfera relaxată și te bucuri de timp împreună —
          exact în ritmul grupului tău.
        </p>
        <button
          @click="toAbout"
          type="button"
          class="btn btn-purple hover:bg-bookmark-white hover:text-black"
        >
          Află mai multe
        </button>
      </div>
    </div>
    <!-- Rounded Rectangle -->
    <div
      class="hidden lg:block overflow-hidden bg-ro-gray rounded-r-full absolute h-60 w-2/4 -bottom-24 -left-36"
    ></div>
  </div>

  <!-- Feature #2 -->
  <div class="relative mt-36 lg:mt-56">
    <div class="container flex flex-col lg:flex-row-reverse items-center justify-center gap-x-24">
      <!-- Image -->
      <div class="flex flex-1 justify-center z-10 mb-10 lg:mb-0">
        <img
          class="w-5/6 h-5/6 sm:w-3/4 sm:h-3/4 md:w-full md:h-full"
          src="../assets/illustrations/soleta.png"
          alt="Căsuța tip șoletă"
        />
      </div>
      <!-- Content -->
      <div class="flex flex-1 flex-col items-center lg:items-start">
        <h1 class="text-3xl text-bookmark-blue">Căsuța tip șoletă – inima centrului</h1>
        <p class="text-bookmark-grey my-4 text-center lg:text-left sm:w-3/4 lg:w-full">
          Spațiu luminos, mult lemn și terasă generoasă sub pergolă. Aici ne strângem pentru ateliere,
          pauze lungi la cafea sau seri liniștite. Designul e gândit pentru confort și simplitate:
          aerisit, cald, ușor de folosit, cu toate dotările la îndemână.
        </p>
        <button
          @click="toAbout"
          type="button"
          class="btn btn-purple hover:bg-bookmark-white hover:text-black"
        >
          Află mai multe
        </button>
      </div>
    </div>
    <!-- Rounded Rectangle -->
    <div
      class="overflow-hidden hidden lg:block bg-ro-gray rounded-l-full absolute h-60 custom-width-class -bottom-14 right-0"
    ></div>
  </div>

  <!-- Feature #3 -->
  <div class="relative mt-36 lg:mt-56">
    <div class="container flex flex-col lg:flex-row items-center justify-center gap-x-24">
      <!-- Image -->
      <div class="flex flex-1 justify-center z-10 mb-10 lg:mb-0">
        <img class="w-3/4 h-3/4 md:w-full md:h-full" src="../assets/illustrations/main.png" alt="Hiking, e-bike și enduro" />
      </div>
      <!-- Content -->
      <div class="flex flex-1 flex-col items-center lg:items-start">
        <h1 class="text-3xl text-bookmark-blue">Afară, în ritmul tău</h1>
        <p class="text-bookmark-grey my-4 text-center lg:text-left sm:w-3/4 lg:w-full">
          În jurul nostru ai poteci ușoare spre viewpoint-uri, trasee e-bike pentru plimbări fără efort
          și rute enduro dedicate pentru cei experimentați. Alegem împreună distanța și nivelul,
          ținem cont de sezon și de vreme, iar siguranța rămâne prioritară — ca să fie o zi frumoasă,
          nu o cursă.
        </p>
        <button
          @click="toAbout"
          type="button"
          class="btn btn-purple hover:bg-bookmark-white hover:text-black"
        >
          Află mai multe
        </button>
      </div>
    </div>
    <!-- Rounded Rectangle -->
    <div
      class="hidden lg:block overflow-hidden bg-ro-gray rounded-r-full absolute h-60 w-2/4 -bottom-24 -left-36"
    ></div>
  </div>
</section>

  <FooterSection />
</template>

<style>
.custom-width-class {
  width: calc(50% - 144px);
}
</style>
