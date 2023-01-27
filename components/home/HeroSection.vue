<template>
  <section class="hero-section">
    <v-container>
      <v-stack
        justify="space-between"
        md-direction="column-reverse"
        md-align="center"
        class="position-relative"
      >
        <v-stack direction="column" class="hero-content-container">
          <v-heading :level="1" class="hero-title">
            <div>Ligo AI</div>            
          </v-heading>
          <v-stack direction="column">
            <app-section-descriptor
              description="Connecting businesses with the power of artificial intelligence."
              class="hero-description"
            />

            <v-stack align="center" gap="1.5rem" sm-gap="1rem" wrap>
              <a href="" target="_blank">
                <v-button label="Primary BTN" label-transform="uppercase" />
              </a>
              <a :href="LIGO_AI_URL" target="_blank">
                <v-button
                  variant="outline"
                  label="TEST BTN"
                  label-transform="uppercase"
                  class="secondary-button"
                />
              </a>

            </v-stack>

          </v-stack>

        </v-stack>
        

     
      </v-stack>



    </v-container>

  </section>
</template>

<script>






const LIGO_AI_URL = process.env.LIGO_AI_BOOK_DEMO_URL
const LIGO_AI_DASHBOARD_URL = process.env.LIGO_AI_DASHBOARD_URL

export default {
  name: 'HeroSection',


  data() {
    return {
      isIntroPlaying: false,
      LIGO_AI_URL,
      LIGO_AI_DASHBOARD_URL,

     
    }
  },

}
</script>

<style lang="css" scoped>
@import url('../lib/media-query-helper.css');

.hero-section {
  padding: 0 0 6rem;


  @media (--viewport-small) {
    padding: 0;
    margin-top: 0 !important;
  }
}

.hero-description {
  margin-block: 2rem;
}

.hero-content-container {
  max-width: 38rem;
}

.hero-title {
  margin-block: 0;
  max-width: 12ch;
}
</style>
