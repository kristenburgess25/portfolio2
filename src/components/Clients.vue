<template>
  <app-section :styleclass="styleclass">
    <div class="section-title-wrapper">
      <h1 class="section-title">Work</h1>
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
      styleclass: 'timeline-tile',
    }
  },
  mounted () {
  }
}
</script>

<style lang="css">
</style>
