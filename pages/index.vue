<template>
  <div class="bg-primary">
    <nav class="flex justify-between border-b border-white">
      <div class="p-10 text-white text-xl">
        <p><span class="mr-1 opacity-40">ons</span><span>polderhart</span></p>
      </div>

      <div class="flex">
        <div class="px-10 flex items-center justify-center">
          <svg class="w-8 h-8" fill="none" viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M11 17.5a6.5 6.5 0 1 0 0-13 6.5 6.5 0 0 0 0 13ZM20.4 20.5l-4.9-4.8" stroke="#fff"/></svg>
        </div>

        <div class="px-10 flex items-center justify-center">
          <svg class="w-8 h-8" viewbox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M3 12h18M3 6h18M3 18h18" stroke="#fff" stroke-miterlimit="10"/></svg>
        </div>
      </div>
    </nav>

    <div class="relative " style="height: 42rem">
      <div class="absolute inset-0">
        <div class=" w-full bg-contain bg-no-repeat bg-right h-full" style="background-image: url('/images/ons_polderhart_1.png')"></div>
      </div>

      <div class="container mx-auto pt-48 relative z-10">
        <h1 class="text-white text-4xl w-1/2">
          Zelf meedenken en meebeslissen over de toekomst van het gebied waarin wij werken en wonen.
        </h1>
        <p class="text-white font-light opacity-50 mt-4">
          Ons Polderhart is een coöperatie van huishoudens in het gebied rondom Wildveldseweg, Gerverscop en Rodendijk.
        </p>

        <div class="mt-4">
          <button class="bg-secondary rounded-full py-3 px-5 mr-4">
            Onze verhalen
          </button>
          <button class="bg-white bg-opacity-25 py-3 px-5 rounded-full text-white">
            Over de coöperatie
          </button>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
