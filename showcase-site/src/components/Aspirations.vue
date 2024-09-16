<template>
    <section class="aspirations">
      <h2>✨ Professional Aspirations</h2>
      <p>{{ aspirations }}</p>
    </section>
</template>
  
<script>
  export default {
    name: 'AppAspirations',
    props: {
      aspirations: {
        type: String,
        required: true
      }
    }
  }
</script>
  
<style scoped lang="scss">
  .aspirations {
    margin-bottom: 2rem;
  
    h2 {
      margin-bottom: 1rem;
    }
  
    p {
      font-style: italic;
      text-align: justify;
    }
  }
</style>