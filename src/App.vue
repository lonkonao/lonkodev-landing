<template>
  <div class="min-h-screen bg-fixed bg-center bg-repeat text-white font-mono"
    :style="{ backgroundImage: 'url(/src/assets/bg-grid.png)' }">

    <div class="flex flex-col items-center justify-center py-10 px-4 text-center space-y-6">

      <!-- LOGO -->
      <img src="/src/assets/lonkodev-logo.png" alt="Lonkodev Logo" class="w-40 h-auto" />

      <p class="max-w-2xl text-lg leading-relaxed text-orange-400">
        Ingeniero en informática y docente en tecnologías digitales.
        Enseño, creo y automatizo soluciones en programación, IA, cloud, ciberseguridad, robótica y más.
        Si algo se puede mejorar con código, lo hago. Y si vale la pena aprenderlo, lo comparto.
      </p>

      <div class="w-full max-w-md space-y-3">
      </div>
    </div>

    <footer class="mt-10 text-center text-sm text-gray-400 pb-6">
      <p>Hecho con 💻 por Lonkodev — Chile</p>
      <p>Donde se enseña en serio y sin chamullo.</p>
    </footer>
  </div>
</template>

<script setup>
</script>

<style scoped></style>
