<template>
  <header>
    <div class="container">
      <div class="header-logo">
        <img src="@/assets/img/logo.png" alt="Avada Forum">
      </div>
      <div class="header-nav">
        <ul class="nav-items">
          <li v-for="(link, index) in links" :key="index" class="nav-item" :class="(link.active) ? 'active' : null">
            <a :href="link.url">{{ link.text }}</a>
          </li>
        </ul>
        <button>JOIN US</button>
        <i class="fas fa-search"></i>
      </div>
    </div>
  </header>
</template>

<script>
import Links from '@/data/Links.js'
export default {
    name: 'Header',
    data(){
        return{
            links: Links.headerLinks
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/general";
header {
  width: 100%;
  height: 60px;
  background-color: $eastern-blue;
  .container {
    height: 100%;
    width: $container;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .header-logo {
      height: 70%;
      img{
        height: 100%;
      }
    }
    .header-nav {
      height: 100%;
      width: 60%;
      display: flex;
      align-items: center;
      .nav-items {
        height: 100%;
        display: flex;
        align-items: center;
        list-style: none; 
        .nav-item {
          margin: 0 10px;
          a{
            text-decoration: none;
            color: $white;
            font-size: $small;
          }
          // &.active{
          //   left: 40px;
          //   width: 0; 
          //   height: 0; 
          //   border-left: 5px solid transparent;
          //   border-right: 5px solid transparent;
          //   border-top: 5px solid black;
          //   position: relative;
          // }
        }
      }
      button {
        padding: 5px 15px;
        background-color: $shark;
        color: $white;
        border: none;
        font-weight: $bold;
        font-size: $small;
        margin: 0 10px;
        cursor: pointer; 
      }
      i {
        color: $white;
        font-size: $small;
        margin-left: 10px;
        cursor: pointer;
      }
      button:hover {
        transform: scale(1.2);
      }
      i:hover {
        font-size: $big;
      }
    }
  }
}
</style>