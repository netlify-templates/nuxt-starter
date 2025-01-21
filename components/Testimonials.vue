<script setup>
const props = defineProps({
  title: String,
  description: String,
  items: Array
});
</script>

<template>
  <h2 class="text-3xl font-bold text-center text-zinc-800 sm:text-4xl" v-if="title">
    {{ title }}
  </h2>
  <p class="max-w-3xl mx-auto mt-4 text-lg text-center text-zinc-600" v-if="description">
    {{ description }}
  </p>
  <div class="mt-10 mb-20 sm:gap-8 sm:columns-2 lg:columns-3">
    <blockquote v-for="item in items" class="p-8 mb-8 border-2 border-dashed rounded break-inside-avoid sm:p-12">
      <p class="text-zinc-500" v-if="item.quote">{{ item.quote }}</p>
      <footer class="flex items-center gap-2 mt-4" v-if="item.author">
        <NuxtImg :src="item.author.avatar" :alt="item.author.name" width="64" height="64" class="object-cover w-16 h-16 rounded-full shrink-0"
          v-if="item.author.avatar" />
        <div class="text-sm" v-if="item.author.name || item.author.title">
          <p class="font-bold text-zinc-800" v-if="item.author.name">{{ item.author.name }}</p>
          <p class="text-zinc-500" v-if="item.author.title">{{ item.author.title }}</p>
        </div>
      </footer>
    </blockquote>
  </div>
</template>
