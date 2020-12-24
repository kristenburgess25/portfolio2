<template>
  <app-section :styleclass="styleclass">
    <div class="section-title-wrapper">
      <h1 class="section-title">Clients</h1>
      <div class="title-underline"></div>
    </div>
    <card-list></card-list>
  </app-section>
</template>

<script>
import Section from './Section.vue';
import ClientCardList from './ClientCardList.vue';
export default {
  name: 'Clients',
  components: {
    'app-section': Section,
    'card-list': ClientCardList,
  },
  data () {
    return {
      styleclass: 'projects-tile',
    }
  },
  mounted () {
  }
}
</script>

<style lang="css">
</style>
