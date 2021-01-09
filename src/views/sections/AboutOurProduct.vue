<template>
  <base-section id="about-our-product">
    <base-section-heading
      color="grey lighten-2"
      icon="mdi-vuetify"
      title="About DRAC"
    />

    <v-container>
      <v-row>
        <v-col
          v-for="card in cards"
          :key="card.title"
          cols="12"
          md="6"
        >
          <base-info-card v-bind="card" />
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionAboutOurProduct',

    data: () => ({
      cards: [
        {
          title: 'Our Vision',
          subtitle: '',
          text: 'A just world, devoid of poverty and intolerant of all forms of discrimination',
          callout: 'DR',
        },
        {
          title: 'Our Mission',
          subtitle: '',
          text: 'DRAC works to facilitate the full participation of vulnerable groups especially persons with disabilities and women/girls while promoting and protecting their rights. DRAC works to facilitate the full participation of vulnerable groups especially persons with disabilities and women and girls in all aspects of life by addressing the drivers of discrimination and exclusion.',
          callout: 'AC',
        },
      ],
    }),
  }
</script>
