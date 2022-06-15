<template>
  <nav class="flex justify-between border-b border-white border-opacity-10">
    <div class="p-8 text-white text-xl">
      <p><span class="mr-1 opacity-40">ons</span><span>polderhart</span></p>
    </div>

    <div class="flex">
      <search />

      <div class="px-10 flex items-center justify-center border-l border-white border-opacity-10 border-l">
        <icon name="menu" />
      </div>
    </div>
  </nav>
</template>

<script>
import search from "~/components/search";
export default {
  components: {search}
}
</script>
