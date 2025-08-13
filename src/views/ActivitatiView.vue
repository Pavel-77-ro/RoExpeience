<script setup>
import NavBar from '../components/NavBar.vue'
import FooterSection from '../components/FooterSection.vue'
import { ref, computed } from 'vue'

// Explicit image imports (Vite will fingerprint these)
import imgTbuild from '../assets/activities/tbuild.jpg'
import imgCooking from '../assets/activities/cooking.jpg'
import imgCrafts from '../assets/activities/crafts.jpg'
import imgMovieNight from '../assets/activities/movie_night.jpg'
import imgCampfire from '../assets/activities/campfire.jpg'
import imgPavilion from '../assets/activities/pavilion.jpg'
import imgHiking from '../assets/activities/hiking.jpg'
import imgEbike from '../assets/activities/ebike.jpg'
import imgEnduro from '../assets/activities/enduro.jpg'

const categories = [
  {
    name: 'Indoor',
    color: 'bg-indigo-200 text-indigo-900',
    activities: [
      {
        title: 'Team-Building & Evenimente',
        img: imgTbuild,
        desc: 'Programe “la cheie” pentru companii și grupuri private: jocuri de colaborare, competiții amuzante, escape-challenge și provocări culinare, toate facilitate pentru traineri certificați.',
        details: [
          'Capacitate 5-20 persoane',
          'Durată 2-6 h • personalizabilă',
          'Echipamente audio-video incluse'
        ]
      },
      {
        title: 'Ateliere Culinare',
        img: imgCooking,
        desc: '“Cooking Hobby” - gătiți rețete locale & internaționale în bucătăria noastră complet echipată.',
        details: [
          '2-6 participanți • 2-3 h',
          'Rețete de sezon & opțiuni vegetariene',
          'Varsta minimă 18 ani'
        ]
      },
      {
        title: 'Badminton & Tras cu Arcul',
        img: imgCrafts,
        desc: 'Spațiu dedicat pentru jocuri de badminton și tras cu arcul, cu echipamente de calitate. Ideal pentru distracție activă în grupuri mici.',
        details: [
          '2-4 participanți • 1 h',
          'Echipamente incluse',
          'Copiii ≥ 6 ani pot participa'
        ]
      },
      {
        title: 'Seri de Film în aer liber',
        img: imgMovieNight,
        desc: 'Proiecţii pe ecran tabla interactiva cu sistem audio profesional sub cerul liber. Filme, documentare sau meciuri, la alegere.',
        details: [
          'Max. 10 persoane',
          'Durată 2 h (după apus)',
          'Scaune puf & pături incluse'
        ]
      },
      {
        title: 'Foc la vatra & Story-telling',
        img: imgCampfire,
        desc: 'Seară în jurul vetrei, povești locale, muzică live la chitară și marshmallows la jar.',
        details: [
          '5-10 persoane',
          'Durată 1-2 h',
          'Lemn & accesorii incluse'
        ]
      },
      {
        title: 'Pavilion Chill-Out',
        img: imgPavilion,
        desc: 'Pavilion acoperit pentru luat masa, workshopuri în aer liber sau coffee-break relaxat.',
        details: [
          'Capacitate 15 persoane',
          ' Wi-Fi',
          'Mobilier confortabil inclus'
        ]
      }
    ]
  },
  {
    name: 'Outdoor',
    color: 'bg-emerald-200 text-emerald-900',
    activities: [
      {
        title: 'Ture de Hiking',
        img: imgHiking,
        desc: 'Drumeții ghidate spre Cabana Suru, Creasta Carpatilor sau vaile din zona – panorame alpine și povești despre zona Făgărașului.',
        details: [
          '10-15 km • 5-8 h',
          'Dificultate usoara sau medie',
          'Grup 5-12 persoane',
          'Picnic & ghid local incluse'
        ]
      },
      {
        title: 'Ture e-Bike',
        img: imgEbike,
        desc: 'Circuit asistat electric Turnu Roşu – Boiţa – Podu Olt (35 km) pe drumuri de culme şi sate pitoreşti.',
        details: [
          '3-4 h • Ușor-Mediu',
          'Grup 4-10 persoane',
          'E-bike, cască & instructaj incluse',
          'Reîncărcare & gustare la destinație'
        ]
      },
      {
        title: 'Ture Enduro (motociclete)',
        img: imgEnduro,
        desc: 'Trasee off-road tehnice Turnu Rosu – Valea Sadului / Talmacel, cu urcări stâncoase și coborâri rapide, pentru rideri experimentați.',
        details: [
          '50-80 km • 4-6 h',
          'Nivel Incepator/Intermediar/Avansat',
          'Grup 3-8 persoane',
          'Ghid si combustibil incluse'
        ]
      }
    ]
  }
]

const activeTab = ref('Indoor')
const setTab = (name) => { activeTab.value = name }
const selectedCategory = computed(() => categories.find(c => c.name === activeTab.value))
</script>

<template>
  <NavBar />

  <!-- Header & Toggle -->
  <section class="pt-24 lg:pt-28 pb-12 bg-gradient-to-b from-white via-slate-50 to-ro-gray/40 relative">
    <div class="container mx-auto px-6 text-center animate-fade-in" style="animation-delay:0.15s;">
      <h1 class="font-bold text-3xl md:text-4xl text-bookmark-blue drop-shadow-sm mb-4">Activităţi</h1>
      <p class="max-w-2xl mx-auto text-bookmark-grey text-lg md:text-xl">
        Descoperă toate experienţele pe care le poţi încerca la centrul nostru – fie că preferi confortul indoor,
        fie aventura în aer liber.
      </p>

      <!-- Toggle -->
      <div class="inline-flex mt-8 border border-slate-300 rounded-full overflow-hidden shadow-sm">
        <button
          v-for="cat in categories"
          :key="cat.name"
          @click="setTab(cat.name)"
          class="px-6 py-2 text-sm md:text-base font-medium transition cursor-pointer"
          :class="activeTab === cat.name ? cat.color : 'bg-white text-slate-600 hover:bg-slate-100'"
        >
          {{ cat.name }}
        </button>
      </div>
    </div>
  </section>

  <!-- Activities Grid -->
  <section v-if="selectedCategory" class="py-20 lg:py-28 bg-gradient-to-t from-white via-slate-50 to-ro-gray/40">
    <div class="container mx-auto px-4">
      <div class="grid gap-12 sm:grid-cols-2 lg:grid-cols-3 items-start">
        <article
          v-for="act in selectedCategory.activities"
          :key="act.title"
          class="group bg-white rounded-3xl shadow-md hover:shadow-xl transition-all duration-300 overflow-hidden flex flex-col animate-fade-in-up"
        >
          <img :src="act.img" :alt="act.title" class="h-56 w-full object-cover group-hover:scale-105 transition-transform duration-300" />

          <div class="p-6 flex flex-col flex-1">
            <h3 class="font-semibold text-xl mb-2 text-bookmark-blue">{{ act.title }}</h3>
            <p class="text-bookmark-grey mb-4 flex-1">{{ act.desc }}</p>
            <ul class="text-sm space-y-1 text-slate-600 list-disc list-inside">
              <li v-for="d in act.details" :key="d">{{ d }}</li>
            </ul>
          </div>
        </article>
      </div>
    </div>
  </section>

  <FooterSection />
</template>

<style scoped>
@keyframes fade-in {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}
.animate-fade-in { animation: fade-in 0.5s both; }

@keyframes fade-in-up {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
.animate-fade-in-up { animation: fade-in-up 0.3s both; }
</style>
