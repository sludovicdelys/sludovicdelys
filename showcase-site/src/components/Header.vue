<template>
    <header>
      <h1>{{ name }}</h1>
      <p>{{ title }}</p>
    </header>
</template>
  
<script>
  export default {
    name: 'AppHeader',
    props: {
      name: {
        type: String,
        required: true
      },
      title: {
        type: String,
        required: true
      }
    }
  }
</script>
  
  <style scoped lang="scss">
  header {
    text-align: center;
    margin-bottom: 2rem;
  
    h1 {
      margin-bottom: 0.5rem;
    }
  
    p {
      font-size: 1.2rem;
      color: var(--secondary-color);
    }
  }
  </style>