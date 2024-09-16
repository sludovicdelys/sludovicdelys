<template>
  <div class="portfolio">
    <Header :name="data.name" :title="data.title" />
    <About :about="data.about" />
    <Skills :skills="data.skills" />
    <WorkInProgress :workInProgress="data.workInProgress" />
    <Projects :projects="data.projects" />
    <DeployedProjects :deployedProjects="data.deployedProjects" />
    <Aspirations :aspirations="data.aspirations" />
    <Contact :contactInfo="data.contactInfo" :linkedInUrl="data.linkedInUrl" />
    <Footer :footerText="data.footerText" />
  </div>
</template>

<script>
import { reactive } from 'vue'
import Header from '@/components/SiteHeader.vue'
import About from '@/components/About.vue'
import Skills from '@/components/Skills.vue'
import WorkInProgress from '@/components/WorkInProgress.vue'
import Projects from '@/components/Projects.vue'
import DeployedProjects from '@/components/DeployedProjects.vue'
import Aspirations from '@/components/Aspirations.vue'
import Contact from '@/components/Contact.vue'
import Footer from '@/components/Footer.vue'
import portfolioData from '@/data/portfolioData.js'

export default {
  name: 'AppPortfolio',
  components: {
    Header,
    About,
    Skills,
    WorkInProgress,
    Projects,
    DeployedProjects,
    Aspirations,
    Contact,
    Footer
  },
  setup() {
    const data = reactive(portfolioData)

    return {
      data
    }
  }
}
</script>

<style scoped lang="scss">
@import '@/styles/mixins';

.portfolio {
  @include responsive-container;
}
</style>