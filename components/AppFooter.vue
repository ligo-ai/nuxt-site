<template>
  <footer>
    <v-container>
      <v-stack
        align="center"
        justify="space-around"
        :grow="1"
        class="footer-logo-container"
      >
        <!-- <v-image class="serv-image" path="images/AI-bust.png" />
        <v-image path="images/footer-orbs.svg" class="position-absolute" /> -->
      </v-stack>
            <app-section-descriptor
        title="Contact"
        heading="GET IN TOUCH"
        description="Ligo AI team can be contacted either directly by email or alternatively through our social media channels. To get the fastest response we recommend to reach us on our Discord server where the team members are always online."
        style="max-width: 64rem"
      />
      <v-stack
        justify="space-between"
        md-direction="column"
        md-align="center"
        class="footer-navigation-container"
      >

        <v-stack direction="column">
          <v-text font="sans" :weight="600" class="get-in-touch">
              Write to us
            </v-text>
          <a href="mailto:hello@ligoai.com">
            <v-text font="sans" :weight="600" class="footer-mailing">
              hello@ligoai.com
            </v-text>
          </a>
          <v-stack style="margin-top: 3rem" md-justify="space-evenly">
            <a href="https://twitter.com/igoAIcom" target="_blank">
              <v-image
                path="images/social/twitter.png"
                class="footer-social-link"
                alt="Ligo AI Twitter"
              />
            </a>

            <a
              style="margin-left: 3rem"
              href="https://discord.gg/yuTuSfESza"
              target="_blank"
            >
              <v-image
                path="images/social/discord.png"
                class="footer-social-link"
                alt="Ligo AI Discord"
              />
            </a>
            <a
              style="margin-left: 3rem"
              href="https://t.me.LigoAI"
              target="_blank"
            >
              <v-image
                style="height: 40px"
                path="images/social/github.png"
                class="footer-social-link"
                alt="Ligo AI Github"
              />
            </a>
          </v-stack>

        </v-stack>
        <v-stack
          class="footer-links-container"
          justify="space-between"
          :grow="1"
        >
          <v-stack direction="column" class="footer-links">
            <!-- <a href="/tech/"><v-text>Technology</v-text></a>
            <a href="/about/"><v-text>About</v-text></a> -->
            <!-- <a
              href="/tech/"
              target="_blank"
            >
              <v-text>Technical Paper</v-text>
            </a>
            <a href="/blog/">
              <v-text>Blog</v-text>
            </a>
          </v-stack>
          <v-stack direction="column" class="footer-links">
            <a href="/careers">
              <v-text>Careers</v-text>
            </a> -->
            <!-- <a
              href="https://github.com/ligo-ai/license/blob/main/PRIVACY.md"
              target="_blank"
              ><v-text>Privacy</v-text></a
            > -->

          </v-stack>
        </v-stack>
      </v-stack>
    </v-container>
  </footer>
</template>

<script>
const LIGO_AI_DISCORD_URL = process.env.LIGO_AI_DISCORD_URL
const LIGO_AI_BOOK_DEMO_URL = process.env.LIGO_AI_BOOK_DEMO_URL

export default {
  name: 'AppFooter',
  data() {
    return {
      LIGO_AI_DISCORD_URL,
      LIGO_AI_BOOK_DEMO_URL,
    }
  },
}
</script>

<style lang="css" scoped>
@import url('./lib/media-query-helper.css');

footer {
  background-color: #000;
  background-size: cover;
  overflow-x: hidden;

  @media (--viewport-small) {
    background-color: #000;
    background-size: 100%;
  }
}

.footer-logo-container {
  padding: 0;
  position: relative;

  @media (--viewport-small) {
    padding: 0;
  }
}

.footer-logo {
  margin: 0 auto;
  width: 8rem;
  height: auto;

  @media (--viewport-medium) {
    width: 6rem;
  }
}

.footer-navigation-container {
  padding: 6rem 0;

  @media (--viewport-small) {
    padding: 3rem 0;
  }
}

.footer-links-container {
  max-width: 50%;

  @media (--viewport-medium) {
    width: 100%;
    margin-top: 3rem;
    max-width: unset;
  }
}

.footer-links > * + * {
  margin-top: 3rem;
}

.footer-social-link {
  width: 3rem;
}

a {
  text-decoration: none;
}

.footer-links a * {
  font-family: var(--font-sans);
  font-weight: 500;
  font-size: 1.5rem;
  line-height: 1.875rem;

  @media (--viewport-medium) {
    font-size: 1.125rem;
    line-height: 1.375rem;
  }
}

.footer-mailing {
  color: #fff;
  font-size: 1.5rem;
  line-height: 2.25rem;
}
.get-in-touch {
  font-size: 1.5rem;
  line-height: 2.25rem;
  color: #31c1bf;

  @media (--viewport-medium) {
    font-size: 1.125rem;
    line-height: 1.5rem;
  }
}

@media (--viewport-small) {
  .footer-logo-container > *:first-child {
    width: 40%;
  }

  .footer-logo-container > *:last-child {
    width: 150%;
  }
}

.book-demo-container {
  margin-top: 4rem;
}



.book-demo-description {
  max-width: 21rem;
  line-height: 1.5;
}

.book-demo-btn {
  width: 14rem;
  height: 3.25rem;
  margin-top: 2rem;
}
</style>
