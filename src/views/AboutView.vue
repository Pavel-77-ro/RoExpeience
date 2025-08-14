<script setup>
import NavBar from '../components/NavBar.vue'
import FooterSection from '../components/FooterSection.vue'
</script>

<template>
  <NavBar />

  <!-- Hero -->
  <section class="pt-28 md:pt-40 pb-10 md:pb-16">
    <div class="mx-auto max-w-3xl md:max-w-4xl px-4 text-center">
      <h1 class="text-4xl md:text-5xl font-bold tracking-tight text-bookmark-blue">Despre RoExperience</h1>
      <p class="mt-6 text-lg md:text-xl text-bookmark-grey leading-8 md:leading-9">
        Un loc liniștit în Tara Oltului, gândit pentru timp de calitate. La noi, activitățile indoor simple și plăcute
        se îmbină cu ieșiri relaxante în natură pe poteci locale. Accentul este pe comunicare, siguranță și ritmul potrivit fiecărui grup.
      </p>
    </div>
  </section>

  <!-- Body copy, minimalist, airy -->
  <section class="py-12 md:py-20">
    <div class="mx-auto max-w-3xl md:max-w-4xl px-4 text-center space-y-14 md:space-y-20">
      <div>
        <h2 class="text-2xl md:text-3xl font-semibold text-bookmark-blue tracking-tight">Misiunea noastră</h2>
        <p class="mt-5 text-bookmark-grey leading-8 md:leading-9">
          Oferim experiențe sigure și prietenoase, în care oamenii se reconectează: familie, prieteni, colegi sau clase de elevi.
          Preferăm lucrurile bine făcute, fără grabă și fără artificii. Programăm activități pe îndelete, astfel încât fiecare să își găsească
          ritmul și să plece cu sentimentul unei zile trăite pe bune.
        </p>
      </div>

      <div>
        <h2 class="text-2xl md:text-3xl font-semibold text-bookmark-blue tracking-tight">Ce găsești la noi</h2>
        <p class="mt-5 text-bookmark-grey leading-8 md:leading-9">
          <strong>Indoor</strong>: ateliere tematice culinare în bucătăria noastră echipată, jocuri de badminton & tir cu arcul pentru toate vârstele,
          seri de film în sezonul cald și seri la focul de tabără. Spațiile sunt simple, curate și confortabile, pregătite pentru lucru în grup
          sau pentru timp de relaxare în tihnă.
        </p>
        <p class="mt-5 text-bookmark-grey leading-8 md:leading-9">
          <strong>Outdoor</strong>: includerea de drumeții in cadrul pachetelor de activitati, pe trasee accesibile, din zona Turnu Roșu: Rezervatia de calcare, Zona Alpina, Cabana Suru, etc. . Pentru doritori,
          există și opțiuni de deplasare cu biciclete asistate electric sau motociclete, însă esența rămâne explorarea calmă a locului,
          în siguranță și cu respect pentru natură.
        </p>
      </div>

      <div>
        <h2 class="text-2xl md:text-3xl font-semibold text-bookmark-blue tracking-tight">Spații & dotări</h2>
        <p class="mt-5 text-bookmark-grey leading-8 md:leading-9">
          Spatiu activitati culinare, atelier pentru activități creative, pavilion aerisit pentru lucru în echipă,
          zonă de relaxare în aer liber și vatră de foc. Avem consumabilele necesare atelierelor, echipamente audio-video de bază și Wi-Fi.
        </p>
      </div>

      <div>
        <h2 class="text-2xl md:text-3xl font-semibold text-bookmark-blue tracking-tight">Cum lucrăm</h2>
        <p class="mt-5 text-bookmark-grey leading-8 md:leading-9">
          Ne place să înțelegem scopul vizitei și componența grupului, apoi propunem un program simplu, cu timpi reali pentru pauze și socializare.
          Durata și nivelul fiecărei activități se ajustează în funcție de vârstă, număr de persoane și sezon. Siguranța rămâne prioritară:
          briefing înainte de demararea activitatilor, echipamente verificate și rute alternative dacă vremea se schimbă.
        </p>
      </div>

      <div>
        <h2 class="text-2xl md:text-3xl font-semibold text-bookmark-blue tracking-tight">Pentru cine</h2>
        <p class="mt-5 text-bookmark-grey leading-8 md:leading-9">
          Familii, prieteni, colegi care vor timp împreună, echipe care caută o zi de conectare în afara biroului,
          dar și persoane care vor să cunoască zona într-un ritm calm. Personalizăm conținutul fără a complica lucrurile.
        </p>
      </div>

      <div>
        <h2 class="text-2xl md:text-3xl font-semibold text-bookmark-blue tracking-tight">Unde ne găsești</h2>
        <p class="mt-5 text-bookmark-grey leading-8 md:leading-9">
          Suntem în <strong>Turnu Roșu, jud. Sibiu</strong>, aproape de potecile care urcă spre Munții Făgăraș. Acces facil din DN7/E81,
          parcare în incintă și liniștea unui sat de la poalele munților. Pentru vizite și detalii, consultă pagina de contact.
        </p>
      </div>
    </div>
  </section>

  <FooterSection />
</template>

<style scoped>
/* Minimal, centrat, mai aerisit pe ecrane medii și mari */
</style>
