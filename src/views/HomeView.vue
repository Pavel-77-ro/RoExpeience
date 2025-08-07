<script setup>
import NavBar from '../components/NavBar.vue';
import FooterSection from '../components/FooterSection.vue';
import { useRouter } from 'vue-router';


const router=useRouter()

function toMap(){
  router.push({name: 'contact'})
}

function toAbout(){
  router.push({name: 'about'})
}

</script>

<template>
  <NavBar/>
  <!-- Hero -->
  <section class="relative">
      <div class="container flex flex-col-reverse lg:flex-row items-center gap-12 mt-20 lg:mt-32">
        <!-- Content -->
        <div class="flex flex-1 flex-col items-center lg:items-start">
          <h2 class="text-bookmark-blue text-3xl md:text-4 lg:text-5xl text-center font-semibold lg:text-left mb-6">
            RoExperience
          </h2>
          <p class="text-bookmark-grey text-lg text-center lg:text-left mb-6">
            Actvitati recreative si sportive pentru toti pasionatii de miscare sau pentru oricine vrea .
          </p>
          <div class="flex justify-center flex-wrap gap-6">
            <button type="button" class="btn btn-purple hover:bg-gray-600 transition font-Lucky text-xl md:text-2xl tracking-wider" @click="toMap()">
              Visit Us
            </button>
            
          </div>
        </div>
        <!-- Image -->
        <div class="flex justify-center flex-1 mb-10 md:mb-16 lg:mb-0 z-10">
          <img class="w-5/6 h-5/6 sm:w-3/4 sm:h-3/4 md:w-full md:h-full" src="../assets/illustrations/main.png" alt="" />
        </div>
      </div>
    
    </section>

    <!-- Features -->
    <section class="bg-bookmark-white py-20 mt-28 lg:mt-60 pb-64 relative">
      <!-- Heading -->
      <div class="sm:w-3/4 lg:w-5/12 mx-auto px-2">
        <h1 class="text-3xl text-center text-bookmark-blue">Features</h1>
        <p class="text-center text-bookmark-grey mt-4">
          Our aim is to make it quick and easy for you to write and save your favourite notes. Your files sync between
          your devices so you can access them on the go.
        </p>
      </div>
      <!-- Feature #1 -->
      <div class="relative mt-24 lg:mt-32">
        <div class="container flex flex-col lg:flex-row items-center justify-center gap-x-24">
          <!-- Image -->
          <div class="flex flex-1 justify-center z-10 mb-10 lg:mb-0">
            <img
              class="w-5/6 h-5/6 sm:w-3/4 sm:h-3/4 md:w-full md:h-full"
              src=""
              alt=""
            />
          </div>
          <!-- Content -->
          <div class="flex flex-1 flex-col items-center lg:items-start">
            <h1 class="text-3xl text-bookmark-blue">Writting in one click</h1>
            <p class="text-bookmark-grey my-4 text-center lg:text-left sm:w-3/4 lg:w-full">
              Organize your notes however you like. Our simple and intuitive interface gives you complete control
              over how you manage your records.
            </p>
            <button @click="toAbout" type="button" class="btn btn-purple hover:bg-bookmark-white hover:text-black">More Info</button>
          </div>
        </div>
        <!-- Rounded Rectangle -->
        <div
          class="
            hidden
            lg:block
            overflow-hidden
            bg-ro-gray
            rounded-r-full
            absolute
            h-60
            w-2/4
            -bottom-24
            -left-36
          "
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
              alt=""
            />
          </div>
          <!-- Content -->
          <div class="flex flex-1 flex-col items-center lg:items-start">
            <h1 class="text-3xl text-bookmark-blue">Simple Editor</h1>
            <p class="text-bookmark-grey my-4 text-center lg:text-left sm:w-3/4 lg:w-full">
              Our lightweight but efficient text editor will make sure you can customize you notes on the go and preserve the options.
            </p>
            <button @click="toAbout" type="button" class="btn btn-purple hover:bg-bookmark-white hover:text-black">More Info</button>
          </div>
        </div>
        <!-- Rounded Rectangle -->
        <div
          class="
            overflow-hidden
            hidden
            lg:block
            bg-ro-gray
            rounded-l-full
            absolute
            h-60
            custom-width-class
            -bottom-14
            right-0
          "
        ></div>
      </div>
      <!-- Feature #3 -->
      <div class="relative mt-36 lg:mt-56">
        <div class="container flex flex-col lg:flex-row items-center justify-center gap-x-24">
          <!-- Image -->
          <div class="flex flex-1 justify-center z-10 mb-10 lg:mb-0">
            <img
              class="w-5/6 h-5/6 sm:w-3/4 sm:h-3/4 md:w-full md:h-full"
              src=""
              alt=""
            />
          </div>
          <!-- Content -->
          <div class="flex flex-1 flex-col items-center lg:items-start">
            <h1 class="text-3xl text-bookmark-blue">Access your Notes</h1>
            <p class="text-bookmark-grey my-4 text-center lg:text-left sm:w-3/4 lg:w-full">
              Easily have your notes and folders at your disposal. Just save your changes before closing the app and access them from anywhere.
            </p>
            <button @click="toAbout" type="button" class="btn btn-purple hover:bg-bookmark-white hover:text-black">More Info</button>
          </div>
        </div>
        <!-- Rounded Rectangle -->
        <div
          class="
            hidden
            lg:block
            overflow-hidden
            bg-ro-gray
            rounded-r-full
            absolute
            h-60
            w-2/4
            -bottom-24
            -left-36
          "
        ></div>
      </div>
    </section>
  <FooterSection/>
</template>

<style>
.custom-width-class {
  width: calc(50% - 144px);
}


</style>