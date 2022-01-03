<template>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div> -->
  <TopMenu />
  <router-view />
</template>

<script>
import TopMenu from "@/components/Top_Menu.vue";
export default {
  components: {
    TopMenu,
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  outline: none;
  border: none;
  box-shadow: none;
  list-style: none;
  text-decoration: none;
}
#app {
  font-family: Mont Regular, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.primary_button {
  font-family: "Mont Semibold";
  font-size: 18px;
  line-height: 1;
  padding: 20px 64px;
  background-color: #00226f;
  color: white;
  border: none;
  cursor: pointer;
}
.primary_button.small {
  padding: 20px 24px;
}

/* #nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
} */
</style>
