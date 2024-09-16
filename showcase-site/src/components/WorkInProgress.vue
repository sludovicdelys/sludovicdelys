<template>
    <section class="work-in-progress">
      <h2>🔨 Work in Progress</h2>
      <ul>
        <li v-for="(project, index) in workInProgress" :key="index">{{ project }}</li>
      </ul>
    </section>
</template>
  
<script>
  export default {
    name: 'WorkInProgress',
    props: {
      workInProgress: {
        type: Array,
        required: true
      }
    }
  }
</script>
  
<style scoped lang="scss">
  .work-in-progress {
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
        content: '🚧';
        position: absolute;
        left: 0;
      }
    }
  }
</style>