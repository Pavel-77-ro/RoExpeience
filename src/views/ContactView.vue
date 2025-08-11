<script setup>
import NavBar from '../components/NavBar.vue'
import FooterSection from '../components/FooterSection.vue'
</script>

<template>
  <NavBar />

  <!-- Contact Info Section -->
  <section class="bg-bookmark-white py-20">
    <div class="container mx-auto px-4 text-center">
      <h1 class="text-4xl font-semibold text-bookmark-blue mb-4">Contact Us</h1>
      <p class="text-bookmark-grey mb-8">
        Ne-ar face plăcere să ne auzim! Pentru orice întrebări sau informații, nu ezitați să ne
        contactați.
      </p>
      <div class="lg:flex flex-row-reverse gap-16 py-4">
        <!-- Map Embed -->
        <div class="aspect-w-16 aspect-h-9 mb-8 border-2 border-gray-200 rounded overflow-hidden">
          <iframe
            class="w-full h-full"
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d11324.123456789!2d24.499999!3d45.700000!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x475bd1234567890%3A0xabcdef1234567890!2sTurnu%20Ro%C8%99u!5e0!3m2!1sen!2sro!4v1620000000000"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </div>

        <!-- Address Details -->
        <div class="space-y-4 max-w-md mx-auto text-left py-4">
          <div class="flex items-center">
            <span class="material-icons text-purple-500 mr-3">location</span>
            <p class="text-bookmark-blue font-medium">Centru Recreational</p>
          </div>
          <p class="text-bookmark-grey">
            Strada Sebesului Nr.686,<br />
            Turnu Roșu, Județul Sibiu,<br />
            Romania, 555600
          </p>

          <div class="flex items-center">
            <span class="material-icons text-purple-500 mr-3">phone</span>
            <p class="text-bookmark-blue font-medium">Phone</p>
          </div>
          <p class="text-bookmark-grey">+40 745 389 858</p>

          <div class="flex items-center">
            <span class="material-icons text-purple-500 mr-3">email</span>
            <p class="text-bookmark-blue font-medium">Email</p>
          </div>
          <p class="text-bookmark-grey">info@example.com</p>
        </div>
      </div>
    </div>
  </section>

  <FooterSection />
</template>

<style scoped>
/* Aspect ratio utility for Tailwind v3; if using v4 CSS-first, ensure aspect-w/h available */
.aspect-w-16 {
  position: relative;
  width: 100%;
}
.aspect-h-9 {
  padding-bottom: calc(9 / 16 * 100%);
}
.aspect-w-16 > iframe,
.aspect-h-9 > iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>
