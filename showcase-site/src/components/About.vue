<template>
    <section class="about">
      <h2>🌍 About Me</h2>
      <p>{{ about }}</p>
    </section>
</template>
  
<script>
  export default {
    name: 'AppAbout',
    props: {
      about: {
        type: String,
        required: true
      }
    }
  }
</script>
  
<style scoped lang="scss">
  .about {
    margin-bottom: 2rem;
  
    h2 {
      margin-bottom: 1rem;
    }
  
    p {
      text-align: justify;
    }
  }
</style>