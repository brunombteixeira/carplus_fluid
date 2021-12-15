<template>
  <section class="key_selling">
    <h2 class="title">O que nos diferencia</h2>
    <div class="ksp_wrapper">
      <div class="ksp">
        <div class="square"></div>
        <div class="line"></div>
        <div class="content">
          <h3>Test-drive</h3>
          <span
            >Lorem Ipsum is simply dummy text of the printing and typesetting
            industry.</span
          >
        </div>
      </div>
      <div class="ksp">
        <div class="square"></div>
        <div class="line"></div>
        <div class="content">
          <h3>300 Pontos de Check-up</h3>
          <span
            >Lorem Ipsum is simply dummy text of the printing and typesetting
            industry.</span
          >
        </div>
      </div>
      <div class="ksp">
        <div class="square"></div>
        <div class="line"></div>
        <div class="content">
          <h3>2 anos de garantia</h3>
          <span
            >Lorem Ipsum is simply dummy text of the printing and typesetting
            industry.</span
          >
        </div>
      </div>
      <div class="ksp">
        <div class="square"></div>
        <div class="line"></div>
        <div class="content">
          <h3>Test-drive</h3>
          <span
            >Lorem Ipsum is simply dummy text of the printing and typesetting
            industry.</span
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "KSP",
};
</script>

<style lang="scss" scoped>
section {
  margin-bottom: 112px;
}
.title {
  font-family: "Mont Semibold";
  font-size: clamp(24px,2.08vw,40px);
  line-height: 1.275;
  text-align: center;
  margin-bottom: clamp(48px,3.33vw,64px);
}
.ksp_wrapper {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  grid-gap: 16px;
  margin: 0 64px;
}
@media only screen and (max-width: 600px) {
  .ksp_wrapper {
    margin: 0 16px;
  }
}
.ksp {
  padding: 40px;
  box-shadow: 0px 1px 3px -1px rgba(0, 0, 0, 0.3),
    0px 2px 5px -1px rgba(50, 50, 93, 0.25);
  border-radius: 4px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  text-align: center;
  .square {
    background-color: #c4c4c4;
    margin: 0 auto;
    width: 120px;
    height: 120px;
  }
  .line {
    height: 1px;
    background-color: #eaeaea;
    margin: 48px 0 48px;
  }
  h3 {
    font-family: "Mont Semibold";
    font-size: clamp(24px, 1.6vw, 32px);
    line-height: 1.3;
    color: #00226f;
    margin-bottom: 16px;
  }
  span {
    font-family: "Mont Regular";
    font-size: 16px;
    line-height: 1.25;
    color: #808080;
  }
}
</style>
