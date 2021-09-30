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
    <!-- section latest-news -->
    <section class="latest-news">
      <div class="container">
        <p class="title">PHASELLUS EGET METUS</p>
        <h2>All the latest news</h2>
        <div class="line"></div>
        <div class="news-image">
          <div class="news">
            <img src="../assets/img/post_feat_img_25-320x202.jpg" alt="Primo articolo">
            <h5 class="news-title">Morbi vitae dui euismod vulputate sollicitudin</h5>
            <p class="subtitle">October 11th, 2015 | <span class="black">2 Comments</span></p>
            <p class="news-text">Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis.Aenean dictum vitae nisl</p>
          </div>
          <div class="second news">
            <img src="../assets/img/post_feat_img_24-320x202.jpg" alt="Primo articolo">
            <h5 class="news-title">Vivamus pellenteque, felis quis varius</h5>
            <p class="subtitle">October 11th, 2015 | Comments off</p>
            <p class="news-text">Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis.Aenean dictum vitae nisl</p>
          </div>
          <div class="news">
            <img src="../assets/img/post_feat_img_23-320x202.jpg" alt="Primo articolo">
            <h5 class="news-title">Donec ornare pretium eget scelisque justo</h5>
            <p class="subtitle">October 11th, 2015 | Comments off</p>
            <p class="news-text">Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis.Aenean dictum vitae nisl</p>
          </div>
        </div>
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
  .container {
    width: $container;
    margin: 0 auto;
  }
  // section slider
  .slider {
    height: 600px;
    background-image: url('../assets/img/home_slider_bg.jpg');
    background-size: cover;
    .slider-txt {
      position: relative;
      width: 100%;
      padding-left: 13%;
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
    background-color: $description;
    .description-container {
      width: 35%;
      margin: 0 auto;
      padding: 80px 0;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      .text {
        color: $nevada;
        margin: 5px 0;
      }
    }
  }
  .title {
    color: $cape-cod;
    font-weight: $bold;
    font-size: $small;
    margin: 20px 0;
  }
  // section latest-news
  .latest-news {
    margin-top: 70px;
    text-align: center;
    h2 {
      font-size: $more-big;
      margin-bottom: 20px;
    }
    .line {
      background-color: $salmon;
      height: 2px;
      width: 10%;
      margin: auto;
      margin-bottom: 50px;
    }
    .news-image {
      width: 100%;
      .news {
        width: calc(100% / 3 - 40px);
        float: left;
        text-align: start;
        cursor: pointer;
        margin-bottom: 50px;
        img {
          width: 100%;
        }
        h5 {
          font-size: $small-normal;
        }
        .subtitle,
        .news-text {
          color: $nevada;
          font-size: $small;
        }
        .subtitle {
          margin-top: 5px;
          margin-bottom: 10px;
        }
        .black {
          color: $shark;
        }
      } 
      .second {
        margin: 0 20px;
      }
    }
  }
}
</style>