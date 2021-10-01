<template>
  <footer>
    <div class="container">
      <div>
        <span>&copy; Copyright 2012 - 2020 | Avada Theme by <span class="black">Theme Fusion</span> | All Rights Reserved | Powered by <span class="black">WordPress</span></span>
      </div>
      <div class="footer-right">
        <div v-for="(link, index) in links" :key="index" class="footer-item" :class="link.color">
          <a :href="link.url"><i :class="link.text"></i></a>
        </div>
      </div>
    </div>
    <div class="arrow-up">
      <i class="fas fa-chevron-up"></i>
    </div>
  </footer>
</template>

<script>
import Links from '@/data/Links.js'
export default {
    name: 'Footer',
    data(){
        return{
            links: Links.footerLinks
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/general";
footer {
  width: 100%;
  height: 100px;
  .container {
    height: 100%;
    width: $container;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    span {
      color: $nevada;
      font-size: $small;
      .black {
        color: $shark;
      }
    }
    .footer-right {
      display: flex;
      .footer-item {
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        margin: 0 5px;
        height: 40px;
        width: 40px;
        border-radius: 50%;
        a {
          text-decoration: none;
          color: $white;
        }
      }
      .san-marino {
        background-color: $san-marino;
      }
      .boston-blue {
        background-color: $boston-blue;
      }
      .wedgewood {
        background-color: $wedgewood;
      }
      .totem-pole {
        background-color: $totem-pole;
      }
    }
  }
  .arrow-up {
    position: relative;
    left: 95%;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 30px;
    width: 35px;
    color: $white;
    background-color: $cape-cod;
    border-top-left-radius: 3px;
    border-top-right-radius: 3px;
  }
}
</style>