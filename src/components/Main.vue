<script>
import Card from './partials/Card.vue'
import db from '../assets/data/db.json'
  export default {
    components:{
      Card
    },

    data(){
      return{
        db
      }
    }
  }
</script>

<template>

  <main>

    <div class="container d-flex box">

      <Card
        v-for="product in db.products" :key="product.id"
        :card="product"
      />

    </div>

  </main>

</template>

<style lang="scss" scoped>

@use './scss/partial/variables' as *; 

  main{
    .box{
      margin-top: 70px;
      justify-content: center;
      align-items: flex-start;
      flex-wrap: wrap;
    }
  }

</style>

