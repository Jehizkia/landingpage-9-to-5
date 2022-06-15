<template>
  <div class="flex items-center h-full border-l border-white border-opacity-10 overflow-hidden">
    <button class="py-10 pl-10 sm:flex items-center justify-center hidden hover:opacity-70" :class="[active ? 'mr-4' : 'pr-10 ']" @click="toggle">
      <icon name="search" />
    </button>

    <div class="w-0 transition-all" :class="[active ? 'w-64' : 'w-0']">
      <input ref="search" class="bg-transparent text-white focus:outline-none">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      active: false,
    }
  },
  methods: {
    toggle() {
      this.active = !this.active

      if (this.active) this.$refs.search.focus()
    }
  }
}
</script>
