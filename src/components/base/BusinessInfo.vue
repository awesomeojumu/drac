<template>
  <v-theme-provider :dark="dark">
    <div>
      <base-info-card
        title="KEEP IN TOUCH WITH US"
        pace="6"
      >
        <strong>Disability Rights Advocacy Center</strong>
      </base-info-card>

      <base-business-contact dense />
    </div>
  </v-theme-provider>
</template>

<script>
  export default {
    name: 'BaseBusinessInfo',

    props: { dark: Boolean },

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
