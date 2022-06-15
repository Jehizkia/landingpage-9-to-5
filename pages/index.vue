<template>
  <div>
    <div class="bg-primary">
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

      <div class="relative ">
        <div class="absolute inset-0">
          <div class=" w-full bg-contain bg-no-repeat bg-right h-full" style="background-image: url('/images/ons_polderhart_1.png')"></div>
        </div>

        <div class="container px-8 lg:px-48 mx-auto py-40 relative z-10">
          <h1 class="text-white text-4xl lg:text-6xl lg:w-10/12">
            Zelf meedenken en meebeslissen over de toekomst van het gebied waarin wij werken en wonen.
          </h1>
          <p class="text-white text-lg font-light opacity-50 mt-4 lg:w-2/3">
            Ons Polderhart is een coöperatie van huishoudens in het gebied rondom Wildveldseweg, Gerverscop en Rodendijk.
          </p>

          <div class="mt-4 flex space-x-6">
            <default-button>
              Onze verhalen
            </default-button>
            <default-button type="secondary">
              Over de coöperatie
            </default-button>
          </div>
        </div>
      </div>
    </div>

    <div class="container px-8 lg:px-48 mx-auto my-16">
      <tabs
        :tabs="['verhalen', 'nieuws']"
      >

        <template v-slot:verhalen>
          <div class="space-y-24 mt-12">
            <card
              v-for="(story, index) in stories"
              :key="index"
              :title="story.title"
              :description="story.excerpt"
              :link="story.link"
              :image="story.banner"
            />
          </div>
        </template>

        <template v-slot:nieuws>
          <div style="background-color: #445c58" class="text-white p-8 rounded-lg text-center mt-6 font-light text-xl flex justify-center flex-col items-center">
            <p>
              Nog geen nieuws berichten beschikbaar
            </p>
          </div>
        </template>

      </tabs>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      stories: [
        {
          title: 'Ons Polderhart voor een levendig en duurzaam platteland',
          excerpt: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas porta dolor vitae lectus laoreet, nec finibus libero fringilla. Praesent luctus orci non leo volutpat, ac varius lacus tempor. Nam eget tempor elit. Sed at odio lectus. Cras et posuere ipsum, volutpat porta ipsum.',
          link: 'https://www.9to5.software/',
          banner: '/images/groep_op__brug_ 1.png'
        },
        {
          title: 'Maak kennis met Hans en Ragnhild',
          excerpt: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas porta dolor vitae lectus laoreet, nec finibus libero fringilla. Praesent luctus orci non leo volutpat, ac varius lacus tempor. Nam eget tempor elit. Sed at odio lectus. Cras et posuere ipsum, volutpat porta ipsum.',
          link: 'https://www.9to5.software/',
          banner: '/images/hans_en_ragnhild_1.png'
        },
        {
          title: 'Dit is Martin, veehouder en onderdeel van Ons Polderhart',
          excerpt: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas porta dolor vitae lectus laoreet, nec finibus libero fringilla. Praesent luctus orci non leo volutpat, ac varius lacus tempor. Nam eget tempor elit. Sed at odio lectus. Cras et posuere ipsum, volutpat porta ipsum.',
          link: 'https://www.9to5.software/',
          banner: '/images/martin_1_2.png'
        },
        {
          title: 'Ons Polderhart is nu écht een coöperatie',
          excerpt: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas porta dolor vitae lectus laoreet, nec finibus libero fringilla. Praesent luctus orci non leo volutpat, ac varius lacus tempor. Nam eget tempor elit. Sed at odio lectus. Cras et posuere ipsum, volutpat porta ipsum.',
          link: 'https://www.9to5.software/',
          banner: '/images/polder_hart.png'
        }
      ]
    }
  }
}
</script>
