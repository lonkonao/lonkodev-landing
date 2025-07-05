<template>
    <a :href="url" target="_blank" rel="noopener"
        class="block w-full text-left px-6 py-4 rounded-lg border-2 border-orange-500 bg-black/50 text-orange-400 hover:bg-orange-500 hover:text-black font-semibold transition-all duration-200 shadow-md">
        <span class="text-xl">{{ emoji }}</span> {{ label }}
    </a>
</template>

<script setup>
defineProps({
    emoji: String,
    label: String,
    url: String
})
</script>
