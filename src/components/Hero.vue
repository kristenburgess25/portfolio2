<template>
  <app-section id="home" :styleclass="styleclass">

    <div class="banner-container">
        <div class="section-title-wrapper">
        <!-- <h2 class="banner-text"> Kristen Burgess </h2> -->
         <div class="title-underline"></div>
        </div>
    </div>
  </app-section>
</template>

<script>
import Section from './Section.vue';

export default {
  name: 'Hero',
  components: {
    'app-section': Section,
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
    height: auto;
    object-fit: cover;

  }

  .banner-container {
    margin-top: 40px;
    display: flex;
    justify-content: center;
    overflow: hidden;
    width: 100%;
    height: 100vh;
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
