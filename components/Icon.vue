<template functional>
  <div>
    <div v-if="props.name === 'search'">
      <svg :class="[props.width, props.height]" fill="none" viewbox="0 0 22 22" xmlns="http://www.w3.org/2000/svg"><path d="M11 17.5a6.5 6.5 0 1 0 0-13 6.5 6.5 0 0 0 0 13ZM20.4 20.5l-4.9-4.8" stroke="#fff"/></svg>
    </div>

    <div v-if="props.name === 'menu'">
      <svg :class="[props.width, props.height]" viewbox="0 0 22 22" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M3 12h18M3 6h18M3 18h18" stroke="#fff" stroke-miterlimit="10"/></svg>
    </div>


    <div v-if="props.name === 'news'">
      <svg :class="[props.width, props.height]" class="fill-current" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6v4H7V8z" />
      </svg>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name:  {
      required: true,
      type: String
    },
    height: {
      default: 'h-8',
      type: String
    },
    width: {
      default: 'w-8',
      type: String
    }
  }
}
</script>
