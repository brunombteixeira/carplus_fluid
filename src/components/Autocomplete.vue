<template>
  <input
    type="text"
    id="search"
    placeholder="Pesquise por marca, modelo, combustível..."
    v-model="searchTerm"
    :class="size"
  />

  <ul v-if="searchCountries.length">
    <li class="length">
      Showing {{ searchCountries.length }} of {{ countries.length }} results
    </li>
    <li class="item" v-for="country in searchCountries" :key="country.name">
      {{ country.name }}
    </li>
  </ul>
</template>

<script>
import { ref, computed } from "vue";
export default {
  name: "Autocomplete",
  props: {
    size: String,
  },
  setup() {
    let searchTerm = ref("");
    let countries = [
      { name: "United Kingdom", value: "UK" },
      { name: "United States", value: "US" },
    ];

    const searchCountries = computed(() => {
      //console.log("Search Term: " + searchTerm.value);
      if (searchTerm.value === "") {
        return [];
      }

      let matches = 0;

      return countries.filter((country) => {
        if (
          country.name.toLowerCase().includes(searchTerm.value.toLowerCase()) &&
          matches < 10
        ) {
          matches++;
          return country;
        }
      });
    });

    const selectCountry = (country) => {
      selectedCountry.value = country;
      searchTerm.value = "";
    };

    let selectedCountry = ref("");

    return {
      countries,
      searchTerm,
      searchCountries,
      selectCountry,
      selectedCountry,
    };
  },
};
</script>

<style lang="scss" scoped>
input {
  background: white;
  padding: 24px 16px;
  width: 100%;
  color: #02226f;
  font-size: 16px;
  line-height: 1;
  transition: all 0.05s;
  &.small {
    padding: 20px 16px;
  }
  &::placeholder {
    color: #808080;
  }
  &:focus,
  &:not(:empty),
  &:not(:placeholder-shown) {
    box-shadow: inset 0px -2px 0px #02226f;
  }
}
input:not(:focus) + ul {
  display: none;
}
ul {
  list-style: none;
  background: white;
  padding: 24px 16px;
  position: absolute;
  margin-top: 2px;
  width: 100%;
}
li.length {
  font-family: "Mont Semibold";
  font-size: 12px;
  line-height: 1;
  text-transform: uppercase;
  color: #808080;
  margin-bottom: 8px;
}
li.item {
  font-size: 16px;
  line-height: 1;
  color: #333;
  &:not(:last-child) {
    margin-bottom: 8px;
  }
}
</style>
