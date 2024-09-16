<template>
  <div id="app">
    <Header :name="portfolio.name" :title="portfolio.title" />
    <main>
      <AboutMe :about="portfolio.about" />
      <Skills :skills="portfolio.skills" />
      <WorkInProgress :projects="portfolio.workInProgress" />
      <TodayILearned :til="portfolio.til" />
      <Projects :projects="portfolio.projects" />
      <DeployedProjects :projects="portfolio.deployedProjects" />
      <Aspirations :aspirations="portfolio.aspirations" />
      <Contact :contactInfo="portfolio.contactInfo" :linkedInUrl="portfolio.linkedInUrl" />
    </main>
    <Footer :text="portfolio.footerText" />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import AboutMe from './components/AboutMe.vue';
import Skills from './components/Skills.vue';
import WorkInProgress from './components/WorkInProgress.vue';
import TodayILearned from './components/TodayILearned.vue';
import Projects from './components/Projects.vue';
import DeployedProjects from './components/DeployedProjects.vue';
import Aspirations from './components/Aspirations.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';
import portfolioData from './data/portfolioData.js';

export default {
  name: 'App',
  components: {
    Header,
    AboutMe,
    Skills,
    WorkInProgress,
    TodayILearned,
    Projects,
    DeployedProjects,
    Aspirations,
    Contact,
    Footer
  },
  data() {
    return {
      portfolio: portfolioData
    };
  }
};
</script>

<style>
#app {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  line-height: 1.6;
  color: #333;
  max-width: 800px;
  margin: 0 auto;
  padding: 1rem;
}

@media (prefers-color-scheme: dark) {
  body {
    background-color: #1a1a1a;
    color: #f0f0f0;
  }
}

@media print {
  body {
    font-size: 12pt;
  }
}
</style>
