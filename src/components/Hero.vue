<template>
  <app-section :styleclass="styleclass">

    <div class="banner-container">

 
        <!-- <img src="https://i.imgur.com/XizsJ1c.jpg" title="source: imgur.com" /> -->

        <div class="section-title-wrapper">
        <h2 class="banner-text"> Kristen Burgess </h2>
         <div class="title-underline"></div>
        </div>



      <!-- <vue-p5
        @preload="preload"
        @setup="setup"
        @draw="draw"
      >
    </vue-p5> -->
    </div>
  </app-section>
</template>

<script>
import Section from './Section.vue';
import VueP5 from 'vue-p5';

export default {
  name: 'Hero',
  components: {
    'app-section': Section,
    'vue-p5': VueP5,
  },
  data () {
    return {
      styleclass: 'hero-tile',
      img: '',
    }
  },
  methods: {
  },
}
</script>

<style lang="css">
@import url('https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@700;900&display=swap');

  .banner-text {
    position: absolute;
    color: #231b4e;
    top: 10%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-family: 'Roboto Slab', serif;
    font-weight: regular;
    font-size: 3rem;
    margin: 1rem 0 0rem;
    text-align: center;
    letter-spacing: 3px;
  }

  img {
    width: 100vw;
    object-fit: cover;
    height: 700px;

  }

  

  .banner-container {
    display: flex;
    justify-content: center;
    overflow: hidden;
    width: 100%;
    height: 645px;
    position: relative;
    text-align: center;
    background: url('https://i.imgur.com/XizsJ1c.jpg') no-repeat center center fixed;
    background-size: cover;
    /* padding: 200px 0px; */
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;

    
  }
</style>
