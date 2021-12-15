<template>
  <FiltersBar />
  <div class="filters_results-label">Resultados: <b>15</b></div>
  <div class="cars_grid-wrapper">
    <Car v-for="index in 10" :key="index" />
  </div>
</template>

<script>
import FiltersBar from "@/components/Search/Filters_Bar.vue";
import Car from "@/components/Car.vue";
export default {
  name: "Search",
  components: {
    FiltersBar,
    Car,
  },
};
</script>

<style lang="scss" scoped>
.filters_results-label {
  font-family: "Mont Regular";
  font-size: 14px;
  line-height: 1;
  text-transform: uppercase;
  color: #808080;
  margin: 24px 64px 32px;
}
.cars_grid-wrapper {
  margin: 0 64px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
}
@media only screen and (max-width: 600px) {
  .cars_grid-wrapper {
    margin: 0 16px;
    display: flex;
    flex-direction: column;
  }
  .filters_results-label {
    margin: 16px;
  }
}
</style>
