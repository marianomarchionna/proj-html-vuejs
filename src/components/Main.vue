<template>
  <main>
    <!-- section slider -->
    <section class="slider">
      <div class="slider-txt">
        <h1>Tech Forum!</h1>
        <p>Discuss all the latest technology news and trends</p>
        <button>GET AVADA NOW! <i class="fas fa-chevron-right"></i></button>
      </div>
    </section>
    <!-- section description -->
    <section class="description">
      <div class="description-container">
        <p class="title">AVADA FORUM IS THE PLACE TO BE</p>
        <p class="text">In quis lectus sed leo elementum faucibus in dapibus dictum.</p>
        <p class="text">Nulla molestie tortor nec lectus venenatis, sed blandit dui finibus.</p>
        <p class="text">dolor at, bibendum purus. Donec vehicula nec tortor ac finibus.</p>
      </div>
    </section>
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
  // section slider
  .slider {
    height: 600px;
    background-image: url('../assets/img/home_slider_bg.jpg');
    background-size: cover;
    .slider-txt {
      position: relative;
      width: 100%;
      padding-left: 15%;
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
  // section description
  .description {
    width: 100%;
    height: 300px;
    background-color: $description;
    .description-container {
      width: 35%;
      height: 100%;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      .title {
        color: $cape-cod;
        font-weight: $bold;
        font-size: $small;
        margin: 20px 0;
      }
      .text {
        color: $nevada;
        margin: 5px 0;
      }
    }
  }
}
</style>