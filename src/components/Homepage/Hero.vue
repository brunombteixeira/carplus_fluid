<template>
  <section class="hero">
    <div class="grid_wrapper">
      <div class="content_block">
        <h1 class="title">{{ this.text }}</h1>
        <Hero_Search />
      </div>
    </div>
  </section>
</template>

<script>
import Hero_Search from "@/components/Homepage/Hero_Search.vue";
export default {
  name: "Hero",
  props: {
    text: String,
  },
  components: {
    Hero_Search,
  },
};
</script>

<style lang="scss" scoped>
.grid_wrapper {
  display: grid;
  grid-template-columns: repeat(12, [col-start] 1fr);
  gap: 16px;
  margin: 0 16px;
}
.hero {
  background-color: #c4c4c4;
  padding-top: clamp(132px, 8.3vw, 160px);
  padding-bottom: clamp(132px, 8.3vw, 160px);
}
.content_block {
  grid-column: col-start 4 / span 6;
  h1 {
    font-family: "Mont Bold";
    font-size: clamp(32px, 3vw, 56px);
    line-height: 1.3;
    text-align: center;
    color: white;
    margin-bottom: 40px;
  }
}
@media only screen and (max-width: 600px) {
  .content_block {
    grid-column: col-start / span 12;
  }
}
</style>
