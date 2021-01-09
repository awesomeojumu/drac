<template>
  <base-section id="theme-features">
    <v-img
      :min-height="minHeight"
      :src="require('@/assets/bkground.jpg')"
      class="white--text"
      gradient="to right, rgba(5, 11, 31, .8), rgba(5, 11, 31, .8)"
    >
      <base-section-heading title="Our Resources" />

      <div>
        <v-container>
          <v-row>
            <v-col
              cols="12"
            >
              <div
                horizontal
              >
                <iframe
                  width="auto"
                  src="https://www.youtube.com/embed/N-R029mucvg"
                  frameborder="0"
                  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                />

                <object
                  width="auto"
                  data="https://drac-ng.org/wp-content/uploads/2017/08/Communique.pdf"
                  type="application/pdf"
                >
                  <iframe
                    width="auto"
                    src="https://docs.google.com/viewer?url=https://drac-ng.org/wp-content/uploads/2017/08/Communique.pdf&embedded=true"
                  />
                </object>
              </div>

              <div>
                <h3>Facts</h3>
                <p>
                  In Nigeria, there exists a very poor resource and database on broad and specific disability issues e.g, status of PWDs health, sexuality and development available to PWDs, researchers, the media and other persons interested in these issues. This poses a major problem when such information or data are needed for reference and/or literature review when programs are being planned or implemented. To fill this gap, DRAC publishes a wide range of resource materials including newsletters, fact sheets, reports and guidelines on Disability that will help all stakeholders better understand Disability Issues, as well as design and evaluate programmes. You may browse and print summaries of these publications or contact info@drac-ng.org  for enquiries and ordering details. <br>

                  DRAC also operates an online resource centre that serves as the resource backbone for program implementers working to advance PWDs SRHR nationally. <br>

                  The resource centre holds over 100 collections covering key concepts of Disability. The online library links to electronic resources available from other websites on these concepts. Clicking on the links below will open an external website.
                </p>
              </div>

              <div
                horizontal
              >
                <iframe
                  width="1180"
                  height="480"
                  src="https://www.youtube.com/embed/N-R029mucvg"
                  frameborder="0"
                  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                />

                <object
                  width="1180"
                  height="400"
                  data="https://drac-ng.org/wp-content/uploads/2017/08/Communique.pdf"
                  type="application/pdf"
                >
                  <iframe
                    width="1000"
                    height="480"
                    src="https://docs.google.com/viewer?url=https://drac-ng.org/wp-content/uploads/2017/08/Communique.pdf&embedded=true"
                  />
                </object>
              </div>

              <div class="imgSlot" />
            </v-col>
          </v-row>
        </v-container>
      </div>
    </v-img>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionResource',

    data: () => ({
      minHeight: 500,
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
