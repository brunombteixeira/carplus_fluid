<template>
  <div class="top_menu">
    <router-link class="logo" to="/"><Logo /></router-link>
    <div class="main_nav">
      <router-link to="/search">Pesquisar Viaturas</router-link>
      <label>Avaliar Retoma</label>
      <label>Como Funciona</label>
      <label>Campanhas</label>
    </div>
    <div class="idgo">
      <IDGO />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Logo from "@/components/Icons/Logo.vue";
import IDGO from "@/components/Icons/IDGO.vue";

export default {
  name: "TopMenu",
  components: {
    Logo,
    IDGO,
  },
};
</script>

<style lang="scss" scoped>
a.logo {
  display: inline-flex;
  svg {
    width: clamp(156px, 13.2vw, 254px);
    height: auto;
  }
}
.top_menu {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  margin: 24px 64px;
}
.main_nav > * {
  font-family: "Mont Semibold";
  font-size: clamp(16px, 0.94vw, 18px);
  line-height: 1;
  color: #00226f;
  cursor: pointer;
  text-decoration: none;
  &:not(:last-child) {
    margin-right: clamp(24px, 2.08vw, 40px);
  }
}
</style>
