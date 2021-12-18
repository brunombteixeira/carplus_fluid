<template>
  <div class="car">
    <div class="image_wrapper">
      <img src="@/assets/cars/FordTransit.png" alt="Ford Transit" />
    </div>
    <div class="content_wrapper">
      <h4 class="model">{{ this.model }}</h4>
      <span class="version">{{ this.version }}</span>
      <div class="properties_wrapper">
        <span class="property">Gasolina</span>
        <span class="property">Manual</span>
        <span class="property">2015</span>
        <span class="property">146.000km</span>
      </div>
      <div class="price_wrapper">
        <div class="monthly_payment">
          <span class="value">320.52€/mês</span>
          <span class="taeg">TAEG: 7.8%</span>
        </div>
        <div class="price">
          <span class="before">36 180€</span>
          <span class="actual">32 540€</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Car",
  props: {
    model: String,
    version: String,
    image: String,
  },
};
</script>

<style lang="scss" scoped>
.car {
  border: 1px solid #eaeaea;
  .image_wrapper {
    background-color: #f4f4f4;
    /* padding-top: 64px;
    padding-bottom: 64px; */
    padding: clamp(56px, 3.33vw, 64px) clamp(24px, 2.34vw, 64px);
    img {
      width: 100%;
      height: auto;
    }
  }
  .content_wrapper {
    padding: clamp(16px, 1.25vw, 24px);
    h4 {
      font-family: "Mont Semibold";
      font-size: clamp(18px, 1.45vw, 21px);
      line-height: 1;
      color: #00226f;
      margin-bottom: 8px;
    }
    .version {
      font-family: "Mont Regular";
      font-size: clamp(14px, 0.85vw, 16px);
      line-height: 1;
      color: #00226f;
      margin-bottom: 32px;
      display: block;
    }
    .properties_wrapper {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      margin-bottom: 40px;
      .property {
        font-family: "Mont Regular";
        font-size: clamp(14px, 0.85vw, 16px);
        line-height: 1.3;
        color: #333;
        &:not(:last-child):after {
          content: "·";
          margin: 0 clamp(8px, 0.83vw, 16px);
        }
      }
    }
    .price_wrapper {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      .monthly_payment {
        display: flex;
        flex-direction: column;
        gap: 8px;
        font-size: clamp(14px, 0.85vw, 16px);
        line-height: 1;
        color: #333;
      }
      .price {
        display: flex;
        flex-direction: column;
        gap: 8px;
        text-align: right;
        .before {
          font-family: "Mont Regular";
          font-size: clamp(18px, 1.45vw, 21px);
          line-height: 1;
          color: #00226f;
          text-decoration: line-through;
        }
        .actual {
          font-family: "Mont Semibold";
          font-size: clamp(28px, 1.77vw, 34px);
          line-height: 1;
          color: #0053ff;
        }
      }
    }
  }
}
/* @media only screen and (max-width: 600px) {
  .car {
    width: 90%;
  }
} */
</style>
