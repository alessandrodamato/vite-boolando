<script>
  export default {
    
  }
</script>

<template>

  <main>

    <div class="container d-flex box">
      <h1>Qui andranno le card...</h1>
    </div>

  </main>

</template>

<style lang="scss" scoped>

@use './scss/partial/variables' as *; 

  main{
    min-height: calc(100vh - 220px); //////////////////////////////////debug
    .box{
      margin-top: 70px;
      justify-content: center;
      align-items: flex-start;
      flex-wrap: wrap;
    }
  }

</style>

