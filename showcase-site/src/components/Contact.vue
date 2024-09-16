<template>
    <section class="contact">
      <h2>📫 How to Reach Me</h2>
      <p>{{ contactInfo }}</p>
      <a :href="linkedInUrl" target="_blank" rel="noopener noreferrer">Connect on LinkedIn</a>
    </section>
</template>
  
<script>
  export default {
    name: 'AppContact',
    props: {
      contactInfo: {
        type: String,
        required: true
      },
      linkedInUrl: {
        type: String,
        required: true
      }
    }
  }
</script>
  
<style scoped lang="scss">
  .contact {
    margin-bottom: 2rem;
  
    h2 {
      margin-bottom: 1rem;
    }
  
    p {
      margin-bottom: 1rem;
    }
  
    a {
      display: inline-block;
      padding: 0.5rem 1rem;
      background-color: var(--secondary-color);
      color: #fff;
      border-radius: 4px;
      transition: background-color 0.3s ease;
  
      &:hover {
        background-color: var(--secondary-color);
        text-decoration: none;
      }
    }
  }
</style>