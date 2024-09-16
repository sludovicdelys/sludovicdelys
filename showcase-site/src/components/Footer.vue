<template>
    <footer class="footer">
      <p>{{ footerText }}</p>
    </footer>
</template>
  
<script>
  export default {
    name: 'AppFooter',
    props: {
      footerText: {
        type: String,
        required: true
      }
    }
  }
</script>
  
<style scoped lang="scss">
  .footer {
    margin-top: 2rem;
    text-align: center;
    font-style: italic;
    border-top: 1px solid var(--secondary-color);
    padding-top: 1rem;
  }
</style>