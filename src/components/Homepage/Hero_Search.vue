<template>
  <div class="search_wrapper">
    <Autocomplete />
  </div>
</template>

<script>
import Autocomplete from "@/components/Autocomplete.vue";
export default {
  name: "Hero_Search",
  components: {
    Autocomplete,
  },
};
</script>

<style lang="scss" scoped>
.search_wrapper {
    position: relative;
    width: 100%;
}
</style>
