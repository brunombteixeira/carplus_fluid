<template>
  <section class="filters_wrapper">
    <span>Filtros</span>
    <Autocomplete size="small" background="beige" />
    <div class="filters_list-wrapper">
      <Select defaultText="Preço e Mensalidade" />
      <Select defaultText="Segmento" />
      <Select defaultText="Marca e Modelo" />
      <Select defaultText="Anos e Quilómetros" />
      <Select defaultText="Combustível" />
    </div>
  </section>
</template>

<script>
import Autocomplete from "@/components/Autocomplete.vue";
import Select from "@/components/Select.vue";
export default {
  name: "FiltersBar",
  components: {
    Autocomplete,
    Select,
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
.filters_list-wrapper {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 16px;
  margin-top: 16px;
}
</style>
