<template>
  <div>
    <button :class="buttonStyle" class="py-3 px-5 rounded-full">
      <slot />
    </button>
  </div>
</template>

<script>
export default {
  props: {
    type: {
      default: 'default',
      type: String
    }
  },
  computed: {
    buttonStyle() {
      if (this.type === 'secondary') {
        return 'bg-white bg-opacity-25 text-white'
      }

      return 'bg-secondary'
    }
  }
}
</script>
