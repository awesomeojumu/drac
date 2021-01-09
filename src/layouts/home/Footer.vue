<template>
  <v-footer
    id="home-footer"
    color="grey darken-4"
    dark
    min-height="72"
  >
    <v-container>
      <v-row>
        <v-col
          cols="12"
          md="6"
        >
          <div class="d-flex flex-wrap justify-md-start justify-center justify-md-none">
            <template v-for="(s, i) in social">
              <a
                :key="i"
                class="white--text pa-1 pa-md-0"
                :href="s.link "
                v-text="s.title"
              />

              <v-responsive
                v-if="i < social.length - 1"
                :key="`divider-${i}`"
                class="mx-4 shrink hidden-sm-and-down"
                max-height="24"
              >
                <v-divider vertical />
              </v-responsive>
            </template>
          </div>
        </v-col>

        <v-col
          class="text-center text-md-right"
          cols="12"
          md="6"
        >
          Copyright &copy; 2020 DRAC Nigeria <br>
          <a
            href="mailto:awesomeojumu@gmail.com"
            style="text-decoration:none"
          ><small>Awesome Ojumu</small></a>
        </v-col>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
  export default {
    name: 'HomeFooter',

    data: () => ({
      social: [
        {
          icon: 'mdi-facebook',
          title: 'Facebook',
          link: 'https://web.facebook.com/DRACNigeria/',
        },
        // {
        //   icon: 'mdi-whatsapp',
        //   title: 'Whatsapp',
        //   link: 'https://twitter.com/DRACNigeria?s=20',
        // },
        {
          icon: 'mdi-twitter',
          title: 'Twitter',
          link: 'https://twitter.com/DRACNigeria?s=20',
        },
        {
          icon: 'mdi-instagram',
          title: 'Instagram',
          link: 'https://www.instagram.com/dracnigeria/',
        },
      ],
    }),
  }
</script>

<style lang="sass">
  #home-footer a
    text-decoration: none
</style>
