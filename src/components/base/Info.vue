<template>
  <v-theme-provider>
    <div>
      <base-img
        :src="require('@/assets/logo.png')"
        contain
        max-width="128"
        min-height="78"
        width="100%"
      />

      <base-title
        size="body-1"
        space="4"
        title="REACH US ANY DAY & AND TIME"
        weight="regular"
      />

      <base-body>
        <!-- Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo pariatur quidem, quis modi iure nihil commodi suscipit, corporis dicta adipisci, voluptatum quia cupiditate. Nulla minus voluptatum nostrum deleniti, asperiores facere. -->
      </base-body>

      <base-btn
        class="mb-12"
        color="white"
        outlined
        href="call: +234 (0) 8115326607"
      >
        More Info
      </base-btn>
    </div>
  </v-theme-provider>
</template>

<script>
  export default {
    name: 'BaseInfo',

    props: {
      title: String,
      dark: Boolean,
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
