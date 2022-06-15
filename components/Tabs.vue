<template>
  <div>
    <div class="flex space-x-4">
      <button
        v-for="(tab, index) in tabs"
        @click="activateTab(tab)"
        :key="`tab-${index}`"
        :class="[active === tab ? 'border-primary': 'border-white opacity-50']"
        class="text-3xl text-primary border-b-2 pb-2 transition-all capitalize">
        {{ tab }}
      </button>
    </div>

    <div v-if="active === tab" v-for="(tab, index) in tabs" :key="`tabView-${index}`">
      <slot  :name="tab" />
    </div>

  </div>
</template>

<script>
export default {
  props: {
    tabs: {
      required: true,
      type: Array
    }
  },
  data() {
    return {
      active: '',
    }
  },

  mounted() {
    this.active = this.tabs[0]
  },

  methods: {
    activateTab(tab) {
      this.active = tab
    }
  }
}
</script>
