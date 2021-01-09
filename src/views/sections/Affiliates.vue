<template>
  <base-section
    id="affiliates"
    class="grey lighten-4"
    space="36"
  >
    <v-container>
      <base-section-heading title="PARTNERS">
        To achieve our goals, we work in partnership with Government, Civil Society Organizations, International Agencies, Religious Bodies, Employers, Schools, Service Providers, Researchers and Disability Advocates.
      </base-section-heading>

      <v-slide-group>
        <template v-for="n in 12">
          <v-slide-item
            :key="n"
            class="align-self-center"
          >
            <base-img
              :src="require(`@/assets/partners/logo-${n}.png`)"
              color="grey"
              contain
              height="40"
              width="128"
            />
          </v-slide-item>

          <v-responsive
            v-if="n < 12"
            :key="`divider-${n}`"
            class="text-center"
            height=""
            width="48"
          >
            <v-divider vertical />
          </v-responsive>
        </template>
      </v-slide-group>
    </v-container>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionAffiliates',
  }
</script>
