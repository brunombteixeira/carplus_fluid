<template>
  <div class="back"><span>Voltar à pesquisa</span></div>
  <div class="header_wrapper">
    <div class="photo_wrapper">
      <div class="rotate_photo"></div>
      <div class="photo_collection">
        <div class="photo_collection-wrapper">
          <div class="photo"></div>
          <div class="photo"></div>
          <div class="photo"></div>
          <div class="photo"></div>
        </div>
      </div>
    </div>
    <div class="information_wrapper">
      <div class="action_wrapper">
        <div class="share_fav-wrapper">
          <div class="share">Partilhar</div>
          <div class="save">Salvar</div>
          <div class="fav">Favoritar</div>
        </div>
        <div class="stats_wrapper">
          <div class="views">14 pessoas a visualizar</div>
          <div class="likes">125 likes</div>
        </div>
      </div>
      <div class="main_info-wrapper">
        <div class="model_info-wrapper">
          <h1 class="model">Renault Traffic</h1>
          <h3 class="version">Premium EV 64kw MY 20’5</h3>
        </div>
        <div class="price_info-wrapper">
          <div class="price">32 540,00€</div>
          <div class="monthly_payment-wrapper">
            <div class="monthly_payment">ou 320.52€/mês | TAEG: 7.8%</div>
            <div class="finance_info">
              96 meses. Entrada inicial: 7 000,00€. Financiamento: 9 505,17€
            </div>
          </div>
          <div class="costs_info">+200€ em despesas contratuais</div>
        </div>
      </div>
      <div class="main_specs-wrapper">
        <div class="main_spec" v-for="index in 6" :key="index">
          <div class="icon"></div>
          <div class="text">Spec Text</div>
        </div>
      </div>
      <div class="anchors_wrapper">
        <div class="anchor">Ver detalhes da viatura</div>
        <div class="anchor">Financiar à medida</div>
        <div class="anchor">Ver certificado de qualidade</div>
      </div>
      <div class="cta_wrapper">
        <button class="interest">Tenho Interesse</button>
        <div class="drop_price">Notificar-me quando baixar o preço</div>
      </div>
    </div>
  </div>
  <Sidesheet />
</template>

<script>
import Sidesheet from "@/components/Product/Sidesheet.vue";
export default {
  name: "Product",
  components: { Sidesheet },
};
</script>

<style lang="scss" scoped>
.back {
  margin: 18px 64px;
  font-family: "Mont Regular";
  font-size: 12px;
  line-height: 1;
  color: #808080;
  cursor: pointer;
  &:before {
    content: "<";
    margin-right: 8px;
  }
}
.header_wrapper {
  margin: 0 64px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  column-gap: 56px;
}
.photo_wrapper > .rotate_photo {
  position: relative;
  width: 100%;
  padding-bottom: 56.25%;
  background: #c4c4c4;
  opacity: 0.5;
  margin-bottom: 16px;
}
.photo_wrapper > .photo_collection > .photo_collection-wrapper {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
  .photo {
    position: relative;
    width: 100%;
    padding-bottom: 56.25%;
    background: #c4c4c4;
    opacity: 0.5;
  }
}
.information_wrapper > .action_wrapper {
  display: flex;
  justify-content: space-between;
  align-content: center;
  margin-bottom: clamp(32px, 3.75vw, 72px);
  .share_fav-wrapper {
    display: flex;
    align-content: center;
    gap: 24px;
    font-family: "Mont Regular";
    font-size: 14px;
    line-height: 1;
    color: #333;
    & > * {
      cursor: pointer;
    }
  }
  .stats_wrapper {
    display: flex;
    align-content: center;
    gap: 24px;
    font-family: "Mont Regular";
    font-size: 14px;
    line-height: 1;
    color: #808080;
  }
}
.main_info-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: clamp(32px, 2.5vw, 48px);
  margin-bottom: clamp(48px, 5vw, 96px);
  .model_info-wrapper {
    color: #00226f;
    h1 {
      font-family: "Mont Bold";
      font-size: clamp(28px, 2.08vw, 40px);
      line-height: 1;
      margin-bottom: clamp(4px, 0.42vw, 8px);
    }
    h3 {
      font-family: "Mont Regular";
      font-size: clamp(16px, 1.09vw, 21px);
      line-height: 1;
    }
  }
  .price_info-wrapper {
    text-align: right;
    .price {
      font-family: "Mont Bold";
      font-size: clamp(32px, 2.92vw, 56px);
      line-height: 1;
      color: #0053ff;
      margin-bottom: clamp(4px, 1.25vw, 24px);
    }
    .monthly_payment-wrapper {
      font-family: "Mont Regular";
      margin-bottom: clamp(12px, 1.25vw, 24px);
      .monthly_payment {
        font-size: clamp(16px, 1.09vw, 21px);
        line-height: 1.3;
        color: #333;
      }
      .finance_info {
        font-size: 12px;
        line-height: 1.3;
        color: #808080;
      }
    }
    .costs_info {
      font-family: "Mont Regular";
      font-size: 13px;
      line-height: 1;
      color: #808080;
      text-transform: uppercase;
    }
  }
}
.main_specs-wrapper {
  display: flex;
  flex: wrap;
  justify-content: space-between;
  align-content: center;
  margin-bottom: 40px;
  .main_spec {
    display: flex;
    flex-direction: column;
    align-items: center;
    .icon {
      width: 32px;
      height: 32px;
      background: #c4c4c4;
      margin-bottom: 16px;
    }
    .text {
      font-family: "Mont Semibold";
      font-size: clamp(14px, 0.83vw, 16px);
      line-height: 1;
      color: #333;
    }
  }
}
.anchors_wrapper {
  display: flex;
  justify-content: space-between;
  flex-grow: 1;
  padding: 20px 0;
  border-bottom: 1px solid #eaeaea;
  border-top: 1px solid #eaeaea;
  .anchor {
    font-family: "Mont Semibold";
    font-size: 14px;
    line-height: 1.3;
    color: #808080;
    cursor: pointer;
  }
}
.cta_wrapper {
  margin-top: 40px;
  .interest {
    font-family: "Mont Semibold";
    font-size: 22px;
    line-height: 1;
    width: 100%;
    padding: 21px 0;
    background: #0053ff;
    color: #fff;
    margin-bottom: clamp(24px, 2.08vw, 40px);
    cursor: pointer;
  }
  .drop_price {
    font-family: "Mont Semibold";
    font-size: clamp(14px, 0.94vw, 18px);
    line-height: 1;
    color: #6497ff;
    text-decoration: underline;
    cursor: pointer;
  }
}
@media only screen and (max-width: 600px) {
  .back {
    display: none;
  }
  .header_wrapper {
    margin: 16px 16px;
    display: flex;
    flex-direction: column;
  }
  .photo_wrapper {
    margin-bottom: 32px;
  }
  .information_wrapper > .action_wrapper {
    flex-direction: column;
    .share_fav-wrapper {
      justify-content: space-between;
      margin-bottom: 16px;
    }
  }
  .main_info-wrapper {
    display: flex;
    flex-direction: column;
    .price_info-wrapper {
      text-align: left;
    }
  }
  .anchors_wrapper {
    flex-direction: column;
    padding: 0;
    border: none;
    .anchor {
      padding: 18px 0;
      border-top: 1px solid #eaeaea;
      &:last-child {
        border-bottom: 1px solid #eaeaea;
      }
    }
  }
  .cta_wrapper {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    padding: 24px 16px;
    background: #fff;
  }
}
</style>
