<template>
  <main>
    <div class="slider">
      <div class="slider-txt">
        <h1>Tech Forum!</h1>
        <p>Discuss all the latest technology news and trends</p>
        <button>GET AVADA NOW! <i class="fas fa-chevron-right"></i></button>
      </div>
    </div>
  </main>
</template>

<script>
export default {
    name: 'Main',
    data(){
        return{
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/general";
main {
  .slider {
    height: 600px;
    background-image: url('../assets/img/home_slider_bg.jpg');
    background-size: cover;
    .slider-txt {
      position: relative;
      left: 15%;
      top: 55%;
      transform: translate(0, -55%);
      h1,
      p, 
      button {
        color: $white;
      }
      h1 {
        font-size: $bigger;
      }
      p {
        margin: 20px 0;
      }
      button {
        background-color: $eastern-blue;
        border: none;
        padding: 10px 25px;
        font-weight: $bold;
        font-size: $small;
        cursor: pointer;
      }
      button:hover {
        transform: scale(1.2);
      }
    }
  }
}
</style>