<script>
  export default {
    
  }
</script>

<template>
  <footer>
    <div class="container d-flex box">

      <div class="d-flex footer-left">
        <h3>Boolando s.r.l.</h3>

        <nav>
          <ul class="d-flex f-size-small">
            <li><a href="#">Informazioni legali</a></li>
            <li><a href="#">Informativa sulla privacy</a></li>
            <li><a href="#">Diritto di recesso</a></li>
          </ul>
        </nav>
      </div>

      <div class="d-flex footer-right">
        <h4 class="f-size-small">Trovaci anche su</h4>

        <nav>
          <ul class="d-flex">
            <li><a href="#"><i class="fa-brands fa-square-twitter"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-square-facebook"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-square-instagram"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-square-pinterest"></i></a></li>
            <li><a href="#"><i class="fa-brands fa-square-youtube"></i></a></li>
          </ul>
        </nav>
      </div>

    </div>
  </footer>
</template>

<style lang="scss" scoped>

@use './scss/partial/variables' as *; 

  footer{
    height: 100px;
    margin-top: 50px;
    background-color: black;
    color: white;
    .box{
      height: 100px;
      justify-content: space-between;
    }
    .footer-left{
      flex-direction: column;
      justify-content: center;
      h3{
        padding: 5px;
        font-size: 1rem;
      }
      ul{
        padding: 5px;
      }
      a{
        padding-right: 10px;
        &:hover{
          text-decoration: underline;
        }
      }
    }
    .footer-right{
      flex-direction: column;
      justify-content: center;
      h4{
        text-align: center;
        padding: 5px;
      }
      a{
        padding-left: 10px;
      }
    }
    nav{
      ul{
        a{
          text-decoration: none;
          color: white;
        }
      }
    }
  }

</style>

