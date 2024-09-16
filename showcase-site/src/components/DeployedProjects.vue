<template>
    <section class="deployed-projects">
      <h2>🚀 Deployed Projects</h2>
      <ul>
        <li v-for="project in deployedProjects" :key="project.name">
          <a :href="project.url" target="_blank" rel="noopener noreferrer">{{ project.name }}</a> | {{ project.tech }}
        </li>
      </ul>
    </section>
</template>
  
<script>
  export default {
    name: 'DeployedProjects',
    props: {
      deployedProjects: {
        type: Array,
        required: true
      }
    }
  }
</script>
  
<style scoped lang="scss">
  .deployed-projects {
    margin-bottom: 2rem;
  
    h2 {
      margin-bottom: 1rem;
    }
  
    ul {
      list-style-type: none;
      padding-left: 0;
    }
  
    li {
      margin-bottom: 0.5rem;
      padding-left: 1.5rem;
      position: relative;
  
      &::before {
        content: '🔗';
        position: absolute;
        left: 0;
      }
    }
  }
</style>