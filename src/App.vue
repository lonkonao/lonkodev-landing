<template>
  <div class="min-h-screen bg-fixed bg-center bg-repeat text-white font-sans"
    :style="{ backgroundImage: 'url(/src/assets/bg-grid.png)' }">
    <div class="flex flex-col items-center justify-center py-10 px-4 text-center space-y-8">

      <!-- LOGO -->
      <img src="/src/assets/lonkodev-logo.png" alt="Lonkodev Logo" class="w-40 h-auto" />

      <!-- FRASE PROFESIONAL -->
      <p class="max-w-2xl text-lg leading-relaxed text-orange-400">
        Profe e ingeniero. Armo soluciones con código, comparto lo que aprendo y automatizo todo lo que puedo.
      </p>

      <!-- SECCIÓN: Redes -->
      <section class="flex justify-center gap-4 mb-6 text-orange-400">
        <a href="https://www.instagram.com/lonkodev/" target="_blank" aria-label="Instagram"
          class="p-3 border-2 border-orange-400 rounded-full hover:bg-orange-500 hover:text-black transition-all">
          <Instagram class="w-5 h-5" />
        </a>

        <a href="https://www.tiktok.com/@lonkodev" target="_blank" aria-label="TikTok"
          class="p-3 border-2 border-orange-400 rounded-full hover:bg-orange-500 hover:text-black transition-all">
          <svg class="w-5 h-5 fill-current" viewBox="0 0 48 48" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M41,14.3c-4.3,0-7.8-3.5-7.8-7.8h-6.4v24.7c0,3.4-2.7,6.1-6.1,6.1s-6.1-2.7-6.1-6.1s2.7-6.1,6.1-6.1c0.7,0,1.4,0.1,2,0.4
      v-6.7c-0.7-0.1-1.3-0.2-2-0.2c-7.1,0-12.8,5.8-12.8,12.8S18.7,42,25.8,42S38.6,36.2,38.6,29V20c1.7,0.9,3.7,1.3,5.7,1.3V14.3z" />
          </svg>
        </a>

        <a href="https://github.com/lonkonao/" target="_blank" aria-label="GitHub"
          class="p-3 border-2 border-orange-400 rounded-full hover:bg-orange-500 hover:text-black transition-all">
          <Github class="w-5 h-5" />
        </a>

        <a href="https://www.linkedin.com/in/lonkodev/" target="_blank" aria-label="LinkedIn"
          class="p-3 border-2 border-orange-400 rounded-full hover:bg-orange-500 hover:text-black transition-all">
          <Linkedin class="w-5 h-5" />
        </a>

        <a href="https://whatsapp.com/channel/0029Vb6GiZY3wtb5gXyzjd1y" target="_blank" aria-label="WhatsApp"
          class="p-3 border-2 border-orange-400 rounded-full hover:bg-orange-500 hover:text-black transition-all">
          <svg class="w-5 h-5 fill-current" viewBox="0 0 32 32">
            <path
              d="M16 2.667c-7.364 0-13.333 5.97-13.333 13.333 0 2.37.634 4.674 1.836 6.7L2.667 29.333 9.68 26.5a13.283 13.283 0 0 0 6.32 1.5c7.364 0 13.333-5.97 13.333-13.333S23.364 2.667 16 2.667Zm0 24a10.61 10.61 0 0 1-5.39-1.47l-.39-.23-3.2 1.31 1.22-3.14-.21-.4a10.71 10.71 0 1 1 8.97 3.93Zm5.82-8.18c-.32-.16-1.91-.94-2.2-1.06-.29-.11-.5-.16-.72.17-.21.31-.83 1.06-1.02 1.28-.19.21-.38.24-.7.08-.32-.16-1.36-.5-2.6-1.6-.96-.86-1.6-1.91-1.78-2.23-.19-.32-.02-.49.14-.64.14-.13.32-.34.48-.51.16-.17.21-.29.32-.49.11-.21.05-.38-.02-.54-.08-.16-.72-1.73-.99-2.37-.26-.64-.53-.55-.72-.55l-.61-.01c-.2 0-.52.07-.79.35-.27.29-1.04 1.02-1.04 2.5s1.06 2.89 1.2 3.09c.14.19 2.07 3.16 5.02 4.43.7.3 1.25.48 1.68.61.71.23 1.36.2 1.87.12.57-.08 1.75-.72 2-1.42.25-.7.25-1.3.17-1.42-.08-.12-.29-.19-.61-.35Z" />
          </svg>
        </a>

      </section>

      <!-- SECCIÓN: Notas -->
      <section class="w-full max-w-md space-y-3 mb-8">
        <h2 class="text-lg text-orange-300 font-bold mb-2">🧠 Notas</h2>
        <LinkButton v-for="(link, index) in notas" :key="'nota-' + index" :emoji="link.emoji" :label="link.label"
          :url="link.url" />
      </section>

      <!-- SECCIÓN: Apuntes -->
      <section class="w-full max-w-md space-y-3 mb-8">
        <h2 class="text-lg text-orange-300 font-bold mb-2">📚 Apuntes</h2>
        <LinkButton v-for="(link, index) in apuntes" :key="'apunte-' + index" :emoji="link.emoji" :label="link.label"
          :url="link.url" />
      </section>

      <!-- SECCIÓN: Web Completa -->
      <section class="w-full max-w-md space-y-3 mb-8">
        <h2 class="text-lg text-orange-300 font-bold mb-2">🌐 Links Interés</h2>
        <LinkButton emoji="🌐" label="Ir a la web completa" url="https://lonkodev.cl" />
      </section>

    </div>

    <!-- FOOTER -->
    <footer class="mt-10 text-center text-sm text-gray-400 pb-6">
      <p>Hecho con 💻 por Lonkodev — Chile</p>
      <p>Donde se enseña en serio y sin chamullo.</p>
    </footer>
  </div>
</template>

<script setup>
import LinkButton from './components/LinkButton.vue'
import { Instagram, Github, Linkedin } from 'lucide-vue-next'
const notas = [
  { emoji: '🧠', label: 'Notas - Patrones de Diseño', url: 'https://patrones.lonkodev.cl/' },
]

const apuntes = [
  { emoji: '📚', label: 'Apuntes - Patrones de Diseño', url: 'https://github.com/lonkonao/PatronesDeDiseno' },
]
</script>

<style scoped>
/* Personalización adicional si quieres */
</style>
