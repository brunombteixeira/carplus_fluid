<template>
  <section class="filters_wrapper">
    <span>Filtros</span>
    <Autocomplete size="small" />
  </section>
</template>

<script>
import Autocomplete from "@/components/Autocomplete.vue";
export default {
  name: "FiltersBar",
  components: {
    Autocomplete,
  },
};
</script>

<style lang="scss" scoped>
section {
  background: #eaeaea;
  margin: 16px 64px 24px;
  padding: clamp(16px, 1.66vw, 32px);
  span {
    display: block;
    font-family: "Mont Semibold";
    font-size: 14px;
    line-height: 1;
    color: #333;
    text-transform: uppercase;
    margin-bottom: 8px;
  }
}
@media only screen and (max-width: 600px) {
  section {
    margin: 16px 16px 24px;
  }
}
</style>
