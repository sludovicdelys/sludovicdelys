<template>
    <section class="skills">
      <h2>🧰 Technologies and Environments</h2>
      <ul>
        <li v-for="(skillSet, category) in skills" :key="category">
          <strong>{{ category }}:</strong> {{ skillSet.join(', ') }}
        </li>
      </ul>
    </section>
</template>
  
<script>
  export default {
    name: 'AppSkills',
    props: {
      skills: {
        type: Object,
        required: true
      }
    }
  }
</script>
  
<style scoped lang="scss">
  .skills {
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
    }
  }
</style>