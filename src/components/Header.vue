<script>
  export default {
    
  }
</script>

<template>

  <header>

    <div class="container d-flex box">

      <nav class="menu categories">
        <ul class="d-flex">
          <li><a href="#">Donna</a></li>
          <li><a href="#">Uomo</a></li>
          <li><a href="#">Bambini</a></li>
        </ul>
      </nav>

      <div class="logo">
        <img src="/img/boolean-logo.png" alt="Logo">
      </div>

      <nav class="menu">
        <ul class="d-flex">
          <li><a href="#"><i class="fa-regular fa-user"></i></a></li>
          <li><a href="#"><i class="fa-regular fa-heart"></i></a></li>
          <li><a href="#"><i class="fa-solid fa-bag-shopping"></i></a></li>
        </ul>
      </nav>

    </div>

  </header>

</template>

<style lang="scss" scoped>

@use './scss/partial/variables' as *; 

  header{
    width: 100%;
    height: 70px;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 999;
    box-shadow: 0 1px 3px grey;
    background-color: $color-primary;
    .box{
      height: 70px;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
    }
    .menu{
      &.categories{
        font-weight: bold;
      }
      a{
        padding: 5px;
        text-decoration: none;
        color: $color-link;
        &:hover{
          text-decoration: underline;
        }
      }
    }
    .logo{
      img{
        width: 130px;
      }
    }
  }

</style>

