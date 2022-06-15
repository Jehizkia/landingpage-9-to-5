<template>
  <div>
    <div class="bg-gray-100 rounded-lg h-80 bg-cover" :style="{'background-image': `url('${image}')`}" />

    <div class="grid md:grid-cols-2 mt-8">
      <div class="text-primary text-3xl pr-12 mb-6 md:mb-0">
        <p style="color: #052520;">
          {{ title}}
        </p>
      </div>

      <div>
        <p class="font-light leading-relaxed text-tertiary">{{ description }}</p>

        <a target="_blank" :href="link" class="bg-secondary rounded-full py-3 px-5 mr-4 mt-4 inline-block">
          Lees verder
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      default: ''
    },
    link: {
      type: String,
      default: null
    },
    image: {
      String,
      default: ''
    }
  }
}
</script>
