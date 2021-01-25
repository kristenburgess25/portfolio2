<template>
  <div class="card-list">
    <div class='card' :class="card.styleclass" v-for="card in helpers" :key="card.title">
      <a :href="card.url" target="_blank">
        <client-card
          :title="card.title"
          :body="card.body"
          :technologies="card.technologies"
        >
        </client-card>
      </a>
    </div>
  </div>
</template>

<script>
import helpers from '../helpers/clients.js'
import ClientCard from './ClientCard.vue'
export default {
  name: 'ClientCardList',
  components: {
    'client-card': ClientCard,
  },
  data () {
    return {
      styleclass: 'card-list',
      helpers,
    }
  },
}
</script>

<style lang="css">
  .card-list {
    align-items: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
  }

  .card {
    border-radius: 0.25rem;
    box-shadow: 2px 2px 8px 0 rgba(0,0,0,.2);
    cursor: pointer;
    flex: 1;
    min-height: 10.9375rem;
    margin: 1rem;
    transform: translateZ(0);
    transition: transform .25s ease-out,-webkit-transform .25s ease-out;
    width: 100%;
  }

  .card > a {
    text-decoration: none;
  }

  .card:hover {
    transform: scale(1.05);
  }

  .grainbridge {
    background-image: url("../images/GB_logo.png");
    background-color: white;
    background-repeat: no-repeat;
    background-size: 90%;
    background-position: center;
  }

    .agex {
    background-image: url("../images/agex-logo.svg");
    background-color: white;
    background-repeat: no-repeat;
    background-size: 90%;
    background-position: center;
  }

  .omnique {
    background-image: url("../images/omnique-logo.png");
    background-color: white;
    background-repeat: no-repeat;
    background-size: 60%;
    background-position: center;
  }

  .d360 {
    background-image: url("../images/dealer-360-logo.jpg");
    background-color: white;
    background-repeat: no-repeat;
    background-size: 90%;
    background-position: center;
  }



  @media screen and (min-width: 48rem) {
    .card-list {
      flex-direction: row;
      flex-wrap: wrap;
      max-width: 70rem;
    }

    .card {
      min-height: 15rem;
      min-width: 20.3rem;
    }
  }

  @media screen and (min-width: 62.5rem) {
    .card {
      min-width: 21.5rem;
    }
  }
</style>
