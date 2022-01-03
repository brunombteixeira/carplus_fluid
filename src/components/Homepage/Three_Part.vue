<template>
  <section class="three_part">
    <div class="grid_wrapper">
      <div class="part part1">
        <h2>Pesquise uma viatura à medida do seu orçamento</h2>
        <div class="search_wrapper">
          <Select defaultText="Mensalidade" />
          <Select defaultText="Entrada Inicial" />
          <button class="search_btn primary_button small">Pesquisar</button>
        </div>
      </div>
      <div class="part part2">
        <h2>Saiba, em 2 minutos, quanto vale a sua viatura de troca</h2>
        <button class="primary_button">Vender o meu carro</button>
      </div>
      <div class="part part3">
        <h2>Campanha Seat Arona, de 20 a 30 de Julho</h2>
      </div>
    </div>
  </section>
</template>

<script>
import Select from "@/components/Select.vue";
export default {
  name: "Three_Part",
  components: {
    Select,
  },
};
</script>

<style lang="scss" scoped>
.grid_wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  margin: 0 16px;
}
@media only screen and (max-width: 600px) {
  .grid_wrapper {
    display: flex;
    flex-direction: column;
  }
}
.three_part {
  margin-top: 16px;
  margin-bottom: 80px;
}
.part {
  padding: clamp(24px, 2vw, 40px);
  background-color: #c4c4c4;
  color: white;
  height: 325px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  h2 {
    font-family: "Mont Bold";
    font-size: clamp(18px, 1.45vw, 28px);
    line-height: 1.3;
    width: 100%;
    max-width: 340px;
  }
}
.search_wrapper {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  gap: 8px;
  justify-content: space-between;
  & > * {
    flex-grow: 1;
  }
}
select {
  font-family: "Mont Regular";
  background: white;
  height: 58px;
  padding: 0 16px;
  outline: none;
  border: none;
  flex-grow: 1;
}
</style>
