<template>
  <div class="card-content">
    <div class="card-title">{{ title }}</div>
    <div class="card-body">{{ body }}</div>
    <div class="card-technologies">{{technologies}}</div>
    <div class="view-project-container">
      <div v-on:click="handleClick(liveUrl)" class="view-project">Live Site →</div>
      <div v-on:click="handleClick(url)" class="view-project">The Code →</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: [
    'title',
    'body',
    'technologies',
    'url',
    'liveUrl'
  ],
  data () {
    return {
    }
  },
  methods: {
    handleClick: function(url) {
      window.open(url, '_blank');
    }
  }
}
</script>

<style lang="css">

  a {
  text-decoration: none;
  }

  .card-content {
    align-items: flex-start;
    color: #fdfcff;
    display: flex;
    flex-direction: column;
    height: 100%;
    justify-content: space-between;
    min-height: 10.9375rem;
  }

  .card-content > div {
    margin: 0.5rem 1.5rem;
  }

  .card-content > div:first-child {
    margin: 1rem 1.5rem 0.5rem;
  }

  .card-content > div:last-child {
    margin: 0.5rem 1.5rem 1rem;
  }

  .card-title {
    font-size: 1.5rem;
    font-weight: 800;
  }

  .card-body {
    font-size: 1.15rem;
  }

  .card-technologies {
    font-size: 0.95rem;
  }

  .view-project-container {
    width: 88%;
    display: flex;
    justify-content: space-between;
  }

  .view-project {
    background: rgba(255, 255, 255, 0.3);
    border-radius: 1rem;
    font-size: 0.875rem;
    padding: 0.25rem 0.75rem;
  }

  .view-project:hover {
    color: #a044ff;
    background-color: white;
    cursor: pointer;
  }

  @media screen and (min-width: 48rem) {
    .card-content {
      min-height: 15rem;
    }
  }
</style>
