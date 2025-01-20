<script setup>
const props = defineProps({
  title: {
    type: String,
    required: false,
  },
  description: {
    type: String,
    required: false,
  },
  buttons: [
    {
      label: {
        type: String,
        required: false,
      },
      url: {
        type: String,
        required: false,
      },
    },
  ],
});
</script>

<template>
  <div class="flex flex-col gap-12 mt-10 mb-20 lg:items-center lg:flex-row">
    <div class="flex-1 w-full">
      <img
        class="rounded-lg"
        src="~/assets/img/hero.jpg"
        alt="Nuxt image"
        loading="eager"
        format="avif"
        width="1000"
        height="1000"
      />
    </div>
    <div class="flex-1 w-full">
      <h1 class="text-4xl font-bold sm:text-5xl text-balance" v-if="title">{{ title }}</h1>
      <p class="max-w-xl mt-4 text-lg text-zinc-600 sm:text-xl" v-if="description">
        {{ description }}
      </p>
      <div class="flex flex-wrap gap-4 mt-8">
        <div v-for="button of buttons">
          <NuxtLink v-if="button.label && button.url" :href="button.url" class="inline-flex px-6 py-3 text-white duration-300 bg-green-600 rounded hover:bg-gray-800 transition-color">{{button.label}}</NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>
