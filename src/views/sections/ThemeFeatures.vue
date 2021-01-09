<template>
  <base-section id="theme-features">
    <v-img
      :min-height="minHeight"
      :src="require('@/assets/bkground.jpg')"
      class="white--text"
      gradient="to right, rgba(5, 11, 31, .8), rgba(5, 11, 31, .8)"
    >
      <base-section-heading title="Theme Features" />

      <div>
        <v-container>
          <v-row>
            <v-col
              v-for="(feature, i) in features"
              :key="i"
              cols="12"
              md="6"
            >
              <div
                v-bind="feature"
                horizontal
              >
                {{ feature.content }}
              </div>

              <div class="imgSlot">
                <v-img
                  :min-height="minHeight"
                  :src="feature.image"
                  class="white--text"
                />
              </div>
            </v-col>
          </v-row>
        </v-container>
      </div>
    </v-img>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionThemeFeatures',

    data: () => ({
      minHeight: 0,
      features: [
        {
          title: 'Pixel Perfect Design',
          icon: 'mdi-fountain-pen-tip',
          content: 'Disability is very common worldwide. The World Health Organization (WHO) estimates that about 1 billion people live with disability worldwide, with about 75% living in the developing countries. In Nigeria, WHO estimates put the number of people with disability at 28 million or approximately 15% of the country’s population. Disability is both a cause and a consequence of poverty. There is a strong relationship between disability and poverty with a cyclical tendency – poverty makes people more vulnerable to disability and disability reinforces and deepens poverty. Disability is an important factor, along with gender, race, ethnicity, etc that interact to impoverish people and keep them poor.People with disabilities (PWDs) are often excluded from the mainstream of the society and hence, may not contribute to the development of the society at all or optimally. It is increasingly being recognized that bringing people with disabilities into the development mainstream will have a significant effect in any plan to cut poverty in the country.',
        },
        {
          image: require('@/assets/drac-2.jpg'),
        },
        {
          image: require('@/assets/drac-6.jpg'),
        },
        {
          title: 'Image Parallax',
          icon: 'mdi-image-size-select-actual',
          content: 'A recent review of disability issues in Nigeria identified many factors why the disability agenda continues to suffer. Notable among them were: the absence of disability discrimination laws, lack of social protection, poor understanding of disability issues by the public, poor access to rehabilitation services and lack of coordinating structure at all levels. While quality of life of PWDs is generally poor, it is common knowledge that women living with disability suffer more. The women are poorer and generally face barriers to full equality and advancement because of such factors as race, age, language, ethnicity, culture, tradition and religion. Persistence of certain cultural, legal and institutional barriers makes women and girls with disabilities victims of two-fold discrimination: as women and as persons with disabilities. Girls and women of all ages with any form of disability are among the more vulnerable and marginalized of society. There is therefore need to take into account and to address their concerns in all policy-making and programming. Special measures are needed at all levels to integrate them into the mainstream of development. Disability Rights Advocacy Center (DRAC) was therefore conceived to provide the much-needed voice and lead a movement that champions a more organized and strategic response to disability issues with a development mindset.',
        },
        {
          title: 'Seo Optimized',
          icon: 'mdi-ice-pop',
        },
        {
          title: '24/7 Support',
          icon: 'mdi-help-circle-outline',
        },
      ],
      computed: {
        minHeight () {
          const height = this.$vuetify.breakpoint.mdAndUp ? '100vh' : '50vh'

          return `calc(${height} - ${this.$vuetify.application.top}px)`
        },
      },
    }),
  }
</script>

<style scoped>
#theme-features{
  padding-top: 20px;
}
</style>
