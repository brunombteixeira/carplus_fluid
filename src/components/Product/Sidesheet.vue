<template>
  <div class="sidesheet_overlay-wrapper">
    <div class="sidesheet_overlay"></div>
    <div class="sidesheet">
      <div class="title_wrapper">
        <span class="title">Formulário de Notificação</span>
        <span class="close">X</span>
      </div>
      <div class="car_selected-wrapper">
        <span class="label">Carro selecionado:</span>
        <div class="card_car-wrapper">
          <div class="photo"></div>
          <div class="content_wrapper">
            <h4 class="model">Renault Captur 1.6</h4>
            <div class="version">E-Tech Híbrido Plug-In Intens 2021</div>
            <div class="finance_wrapper">
              <div class="monthly_payment-wrapper">
                <div class="payment">320.52€/mês</div>
                <div class="taeg">TAEG: 7.8%</div>
              </div>
              <div class="price_wrapper">
                <div class="price">32 540,00€</div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="form_content-wrapper">
        <span
          >Complete as seguintes informações e avisá-lo-emos, quando o preço da
          viatura baixar.</span
        >
        <div class="form_wrapper">
          <div class="form_block-wrapper">
            <div class="title">1. Informação de Contato</div>
            <input type="text" name="name" id="name" placeholder="Nome" />
            <input type="text" name="name" id="name" placeholder="Email" />
            <input type="text" name="name" id="name" placeholder="Telemóvel" />
          </div>
          <div class="form_block-wrapper">
            <div class="title">1. Data e Horário preferencial</div>
            <Select defaultText="Dia de Contacto" />
            <Select defaultText="Data de Contacto" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Select from "@/components/Select.vue";
export default {
  name: "Sidesheet",
  components: {
    Select,
  },
};
</script>

<style lang="scss" scoped>
.sidesheet_overlay-wrapper {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
}
.sidesheet_overlay {
  position: relative;
  width: 100%;
  height: 100%;
  background: #000000;
  opacity: 0.6;
}
.sidesheet {
  position: absolute;
  top: 0;
  right: 0;
  width: 650px;
  height: 100vh;
  background: #fff;
  padding: 40px;
  .title_wrapper {
    display: flex;
    justify-content: space-between;
    align-content: center;
    font-family: "Mont Semibold";
    font-size: 24px;
    line-height: 1;
    margin-bottom: 32px;
    padding-bottom: 40px;
    border-bottom: 1px solid #eaeaea;
    .title {
      color: #00226f;
    }
    .close {
      color: #333;
      cursor: pointer;
    }
  }
}
.car_selected-wrapper {
  margin-bottom: 48px;
  .label {
    display: block;
    font-family: "Mont Regular";
    font-size: 16px;
    line-height: 1;
    color: #333;
    margin-bottom: 16px;
  }
  .card_car-wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr;
    border: 1px solid #eaeaea;
    .photo {
      width: 100%;
      height: 100%;
      background: #eaeaea;
    }
    .content_wrapper {
      padding: 16px;
      .model {
        font-family: "Mont Semibold";
        font-size: 18px;
        line-height: 1;
        margin-bottom: 4px;
        color: #00226f;
      }
      .version {
        font-family: "Mont Regular";
        font-size: 14px;
        line-height: 1;
        margin-bottom: 40px;
        color: #00226f;
      }
      .finance_wrapper {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 24px;
        align-items: center;
        .monthly_payment-wrapper {
          font-family: "Mont Semibold";
          font-size: 14px;
          line-height: 1.3;
          color: #333;
        }
        .price_wrapper > .price {
          font-family: "Mont Semibold";
          font-size: 18px;
          line-height: 1.3;
          text-align: right;
          color: #0053ff;
        }
      }
    }
  }
}
.form_content-wrapper {
  & > span {
    display: block;
    font-family: "Mont Regular";
    font-size: 14px;
    line-height: 1.3;
    color: #333;
    margin-bottom: 40px;
  }
  .form_block-wrapper {
    .title {
      font-family: "Mont Semibold";
      font-size: 16px;
      line-height: 1;
      color: #333;
      margin-bottom: 16px;
    }
    input {
      display: block;
      width: 100%;
      padding: 20px 16px;
      background: #fbfbfb;
      margin-bottom: 16px;
      &:last-child {
        margin: 0;
      }
    }
  }
}
</style>
