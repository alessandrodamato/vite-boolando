<script>
  export default {
    data(){
      return{
        footerLeft:[
          {
            text: 'Informazioni legali',
            link: '#',
          },
          {
            text: 'Informativa sulla privacy',
            link: '#',
          },
          {
            text: 'Diritto di recesso',
            link: '#',
          },
        ],
        footerRight:[
          {
            icon: '<i class="fa-brands fa-square-twitter"></i>',
            link: '#',
          },
          {
            icon: '<i class="fa-brands fa-square-facebook"></i>',
            link: '#',
          },
          {
            icon: '<i class="fa-brands fa-square-instagram"></i>',
            link: '#',
          },
          {
            icon: '<i class="fa-brands fa-square-pinterest"></i>',
            link: '#',
          },
          {
            icon: '<i class="fa-brands fa-square-youtube"></i>',
            link: '#',
          },
        ]
      }
    }
  }
</script>

<template>
  <footer>
    <div class="container d-flex box">

      <div class="d-flex footer-left">
        <h3>Boolando s.r.l.</h3>

        <nav>
          <ul class="d-flex f-size-small">
            <li v-for="(item, index) in footerLeft" :key="`fl-${index}`"><a :href="item.link">{{ item.text }}</a></li>
          </ul>
        </nav>
      </div>

      <div class="d-flex footer-right">
        <h4 class="f-size-small">Trovaci anche su</h4>

        <nav>
          <ul class="d-flex">
            <li v-for="(item, index) in footerRight" :key="`fr-${index}`"><a :href="item.link" v-html="item.icon"></a></li>
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

