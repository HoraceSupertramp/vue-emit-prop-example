<template>
  <div id="app">
    <FiltersParent @change="onFiltersChange"/>
    <MainComp title="Ciao" :selectedValue="selectedValue"/>
  </div>
</template>

<script>
import MainComp from './components/MainComp.vue';
import FiltersParent from './components/FiltersParent.vue';

export default {
  name: 'App',
  data() {
    return {
        selectedValue: 'none',
    };
  },
  components: {
    MainComp,
    FiltersParent
  },
  methods: {
    onFiltersChange(newSelectedValue) {
        this.selectedValue = newSelectedValue;
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
