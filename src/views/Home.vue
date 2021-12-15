<template>
  <Hero text="Compre online e receba a viatura em sua casa" />
  <Three_Part />
  <KSP />
  <CarsList />
</template>

<script>
// @ is an alias to /src
import Hero from "@/components/Homepage/Hero.vue";
import Three_Part from "@/components/Homepage/Three_Part.vue";
import KSP from "@/components/Homepage/KSP.vue";
import CarsList from "@/components/Homepage/CarsList.vue";

export default {
  name: "Home",
  components: {
    Hero,
    Three_Part,
    KSP,
    CarsList,
  },
};
</script>
