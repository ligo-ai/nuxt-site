<template>
  <section>
    <v-container>
      <app-section-descriptor
        title="Services"
        heading="What Ligo AI Solves and Provides"
        description="Making use of machine learning and blockchain technologies, Ligo AI helps your business to enhance cybersecurity, automate tasks, optimize supply chain management, improve customer service, augment your marketing strategies and improve talent management"
        style="max-width: 64rem"
      />
      <div class="overview-features">
        <v-stack
          align="center"
          sm-align="start"
          gap="10rem"
          sm-gap="3rem"
          justify="space-evenly"
        >
          <div class="icon-container">
            <v-image class="serv-image" 
            path="images/ligo-ai-cybersecurity.png" 
            alt="Ligo AI Enhanced Cybersecurity" />
          </div>
          <div class="overview-feature">
            <v-heading :level="2" class="overview-feature-title">
              Enhanced Cybersecurity
            </v-heading>
            <div class="overview-feature-description">
              <v-text
                color="secondary"
                line-height="1.5"
                class="feature-description-text"
              >
              Ligo Artificial Intelligence is an advanced technology solution designed to enhance the security of your business by identifying and proactively preventing cyber threats. 
              By leveraging cutting-edge machine learning algorithms, Ligo AI can analyze large amounts of data and identify potential security vulnerabilities, allowing your 
              organization to take swift action to protect sensitive information and maintain the integrity of your systems. 
              This powerful tool is essential for any business looking to stay ahead of the ever-evolving cyber threat landscape.
              </v-text>
            </div>
          </div>
        </v-stack>
        <v-stack
          align="center"
          sm-align="start"
          gap="10rem"
          sm-gap="3rem"
          justify="space-evenly"
        >
          <div class="overview-feature">
            <div>
              <v-heading :level="2" class="overview-feature-title">
                Talent Management
              </v-heading>
            </div>
            
            <div class="overview-feature-description">
              <v-text
                color="secondary"
                line-height="1.5"
                class="feature-description-text"
              >
              Ligo AI can be used to improve HR and talent management by analyzing
              resumes, job applications, and candidate data to identify top candidates for a position. 
              Our AI tools can also be used to screen resumes, schedule interviews or analyze existing employee data to identify patterns and predict the potential of your employees, helping you to identify high-performers. 
              This can save HR professionals time and reduce the risk of human bias in the hiring process and to create more effective development and training programs. 
              </v-text>
            </div>
          </div>
          <div class="icon-container">
            <v-image class="serv-image"
              path="images/ligo-ai-hr.png"
              alt="Ligo AI Talent Management"
            />
          </div>
        </v-stack>
        <v-stack
          align="center"
          sm-align="start"
          gap="10rem"
          sm-gap="3rem"
          justify="space-evenly"
        >
          <div class="icon-container">
            <v-image class="serv-image"
              path="images/ligo-ai-marketing.png"
              alt="Ligo AI Augmented Marketing"
            />
          </div>
          <div class="overview-feature">
            <div>
              <v-heading :level="2" class="overview-feature-title">
                Augmented Marketing
              </v-heading>
            </div>
            <div class="overview-feature-description">
              <v-text
                color="secondary"
                line-height="1.5"
                class="feature-description-text"
              >
              Ligo AI is providing powerful tools you need to analyze dat and create effective marketing campaigns by leveraging advanced machine learning algorithms (AI).
              Our AI technology can provide your business valuable insights about consumer behavior and preferences, helping you to create a more personalized and effective marketing campaigns by analyzing data and identifying the most effective content and strategies. 
              This can help your business to reach your target audience more effectively and improve the overall marketing ROI.
              </v-text>
              
            </div>
          </div>
        </v-stack>
        <v-stack
          align="center"
          sm-align="start"
          gap="10rem"
          sm-gap="3rem"
          justify="space-evenly"
        >
          <div class="overview-feature">
            <div>
              <v-heading :level="2" class="overview-feature-title">
                Improved Customer Care
              </v-heading>
            </div>
            
            <div class="overview-feature-description">
              <v-text
                color="secondary"
                line-height="1.5"
                class="feature-description-text"
              >
              Ligo AI will improve customer service by providing efficient and personalized support, 
              automating routine tasks, and providing valuable insights for improving customer experiences by building safer dialogue agents
               using AI in the critical area of research and development. A dialogue agent, also known as a conversational agent or chatbot, 
               is a computer program that can engage in a conversation with a human. 
              These agents can be used in a variety of applications, such as your customer service, e-commerce platforms, and personal assistants.
              </v-text>
            </div>
          </div>
          <div class="icon-container">
            <v-image class="serv-image"
              path="images/ligo-ai-customer-care.png"
              alt="Ligo AI Customer Care"
            />
          </div>
        </v-stack>
        
      </div>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'Features',
}
</script>

<style lang="css" scoped>
@import url('../lib/media-query-helper.css');

section {
  padding-bottom: 6rem;

  @media (--viewport-small) {
    padding-bottom: 3rem;
  }
}

.overview-description {
  max-width: 52ch;
  font-size: 1.25rem;

  @media (--viewport-small) {
    font-size: 1rem;
  }
}

.overview-feature {
  max-width: 40rem;
  text-align: left;
}

.overview-features > * {
  margin-top: 6rem;

  @media (--viewport-small) {
    margin-top: 3rem;
  }
}

.overview-feature-title {
  margin: 0;
  font-size: 2.25rem;
  line-height: 1.5;

  @media (--viewport-small) {
    font-size: 1.25rem;
  }
}

.overview-feature-description {
  margin-top: 1.25rem;
}

.feature-description-text {
  font-size: 1.375rem;

  @media (--viewport-small) {
    font-size: 0.875rem;
  }
}
.serv-image{
  max-width: 20vw;
}
.icon-container {
  position: relative;
  overflow: visible;
}

.icon-container::before {
  content: '';
  position: absolute;
  top: -40%;
  left: -40%;
  right: -40%;
  bottom: -40%;
  z-index: -1;
  background: radial-gradient(
    45% 40% at 50% 50%,
    rgba(112, 239, 207, 0.3) 0%,
    rgba(0, 0, 0, 0) 100%
  );
  filter: blur(5px);
}

.icon-container:nth-child(2)::before {
  background: radial-gradient(
    45% 40% at 50% 50%,
    rgba(112, 239, 207, 0.3) 0%,
    rgba(0, 0, 0, 0) 100%
  );
}

.icon-container > * {
  @media (--viewport-medium) {
    width: 10rem;
    margin-top: 1rem;
  }

  @media (--viewport-small) {
    width: 6rem;
    margin-top: 0.5rem;
  }
}
</style>
