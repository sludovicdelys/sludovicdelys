<template>
    <section class="projects">
      <h2>📚 Public Projects</h2>
      <ul>
        <li v-for="project in projects" :key="project.name">
          <strong>{{ project.name }}:</strong> {{ project.description }}
        </li>
      </ul>
    </section>
</template>
  
<script>
  export default {
    name: 'AppProjects',
    props: {
      projects: {
        type: Array,
        required: true
      }
    }
  }
</script>
  
<style scoped lang="scss">
  .projects {
    margin-bottom: 2rem;
  
    h2 {
      margin-bottom: 1rem;
    }
  
    ul {
      list-style-type: none;
      padding-left: 0;
    }
  
    li {
      margin-bottom: 1rem;
      padding-left: 1.5rem;
      position: relative;
  
      &::before {
        content: '📁';
        position: absolute;
        left: 0;
      }
    }
  }
</style>