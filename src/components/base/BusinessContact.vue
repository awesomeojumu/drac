<template>
  <v-theme-provider :dark="dark">
    <div>
      <base-info-card
        :title="title"
        color="primary"
      >
        <slot />
      </base-info-card>

      <template v-for="({ icon, text, title: t }, i) in business">
        <div
          :key="i"
          :icon="icon"
          :outlined="false"
          :title="!dense ? t : undefined"
          color="transparent"
          horizontal
          space="0"
        >
          <!-- Do not use v-html for user -->
          <!-- provided values -->
          <div v-html="text" />
        </div>

        <v-divider
          v-if="i + 1 !== business.length"
          :key="`divider-${i}`"
          class="my-2"
        />
      </template>
    </div>
  </v-theme-provider>
</template>

<script>
  export default {
    name: 'BaseBusinessContact',

    props: {
      dark: Boolean,
      dense: Boolean,
      title: String,
    },

    data: () => ({
      business: [
        {
          icon: 'mdi-map-marker-outline',
          title: 'Address',
          text: 'Plot 690 (AKON HOUSE) Gidado Idris Street, Opposite Family Worship Center, Wuye District, Abuja - Nigeria',
        },
        {
          icon: 'mdi-cellphone',
          title: 'Phone',
          text: '+234 (0) 8115326607',
        },
        {
          icon: 'mdi-email',
          title: 'Email',
          text: 'info@drac-ng.org <br> drac.nigeria@gmail.com',
        },
      ],
    }),
  }
</script>
