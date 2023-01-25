<template>
  <section style="margin-bottom: 10rem">
    <v-container>
      <v-stack justify="space-between">
        <app-section-descriptor
          title="Our team"
          heading="The Ligo AI Builders"
        />
      </v-stack>
      <v-stack
        justify="space-between"
        md-direction="column"
        class="member-container"
        wrap
      >
        <div
          v-for="member in executiveMembers"
          :key="member.name + member.designation"
        >
          <about-team-member :member="member" />
        </div>
      </v-stack>

    </v-container>
  </section>
</template>

<script>
export default {
  name: 'OurTeam',
  data() {
    return {
      executiveMembers: [
        {
          name: 'Adrian Munteanu',
          designation: 'Founder, Lead Backend Developer',
          image: 'adrian',
          links: {
            linkedin: "https://linkedin.com/in/adrian-munteanu85",
            github: "https://github.com/adi-mun",
            twitter: "https://twitter.com/adimun_"
          },
        },
        {
          name: 'Marius Oprea',
          designation: 'Founder, Senior Backend Developer',
          image: 'marius',
          links: {

          },
        },
        {
          name: 'Bogdan Vasile',
          designation: 'Lead Frontend Developer',
          image: 'bogdan',
          links: {

          },
        },
        {
          name: 'Alina Dumitru',
          designation: 'Head of Marketing',
          image: 'alina',
          links: {

          },
        },
        {
          name: 'Cristian Stanciu',
          designation: 'Assistant Developer',
          image: 'cristian',
          links: {

          },
        },
        {
          name: 'Georgiana Stan',
          designation: 'UX/UI Designer',
          image: 'georgiana',
          links: {

          },
        },
      ],


    }
  },

}
</script>

<style lang="css" scoped>
@import url('../lib/media-query-helper.css');

.member-container {
  margin: 1rem 0;
  text-align: center;

  @media (--viewport-medium) {
    text-align: start;
  }
}

.member-container > * {
  margin: 1rem 0;
  flex: 1 0 33%;
}

.other-members {
  max-height: 0;
  opacity: 0;
  overflow: hidden;
  transition: max-height 0.4s, opacity 0.8s;
}

.expanded {
  opacity: 1;
  max-height: 100%;
}

@media (--viewport-medium) {
  .member-container > * + * {
    margin-top: 1rem;
  }
}
</style>
