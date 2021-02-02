<template>
    <div class="nav-container">
    <nav :styleclass="styleclass">
        <!-- <a class="nav-link" href="/#home">Home</a> | -->
        <a class="nav-link" href="/#about">About</a> |
        <a class="nav-link" href="/#work">Work</a> |
        <a class="nav-link" href="/#play">Play</a> |
        <a class="nav-link" href="/#contact">Contact</a>
    </nav>
    <!-- <a href="/#home">
    <img id="logo" src="../../apple-touch-icon.png"/>
    <a/> -->
    <div>
</template>

<script>
import Section from './Section.vue';

export default {
  name: 'Nav',
  components: {
    'app-section': Section,
  },
  data () {
    return {
      styleclass: 'contact-tile',
    }
  }
}
</script>

<style lang="css">

#logo {
    height: 100%;
    width: auto;
    float: right;
    position: absolute;
    right: 0;
    margin: auto 10px;
}


.nav-container {
    display: flex;
    position: fixed; 
    width: 100%;
    top: 0;
    z-index: 100;
    background-color: #2B303A;
    color: #a044ff;
    height: 40px;
    text-decoration: none;
    padding-left: 10px;

}

nav {
    float: left;
    margin: auto 10px;
}



.nav-link {
  text-decoration: none;
  color: white;
  font-family: 'Roboto Slab', serif;
  font-size: 1.1rem;
  margin: 0px 10px;
}

a:hover {
    color: #a044ff;
}

@media (max-width: 500px) {
    #logo {
    visibility: hidden;
    }

    .nav-link {
        font-size: 1rem;
    }
}


</style>
