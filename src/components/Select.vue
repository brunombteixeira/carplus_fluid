<template>
  <div class="select_wrap" :class="isActive ? 'active' : ''">
    <ul class="default_option" @click="clickDefault">
      <li>
        <div class="option pizza">
          <p>{{ this.defaultText }}</p>
        </div>
        <div class="chevron"></div>
      </li>
    </ul>
    <ul class="select_ul">
      <li>
        <div class="option pizza">
          <p>Pizzas</p>
        </div>
      </li>
      <li>
        <div class="option burger">
          <p>Burget</p>
        </div>
      </li>
      <li>
        <div class="option ice">
          <p>Ice Cream</p>
        </div>
      </li>
      <li>
        <div class="option fries">
          <p>Fried Potatoes</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "Select",
  props: {
    defaultText: String,
  },
  setup() {
    const isActive = ref(false);
    const clickDefault = () => {
      isActive.value = !isActive.value;
    };
    return { isActive, clickDefault };
  },
};
</script>

<style lang="scss" scoped>
.select_wrap {
  position: relative;
  font-family: "Mont Regular";
  font-size: 16px;
  line-height: 1;
  color: #808080;
  flex-grow: 1;
  user-select: none;
}

.select_wrap .default_option {
  position: relative;
  background: #fbfbfb;
  cursor: pointer;
  li {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 20px 16px;
    p {
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }
    & > .chevron {
      width: 8px;
      height: 8px;
      margin-left: 8px;
      border: 2px solid;
      border-top-color: currentcolor;
      border-right-color: currentcolor;
      border-bottom-color: currentcolor;
      border-left-color: currentcolor;
      border-color: transparent transparent #555555 #555555;
      transform: rotate(-45deg);
      transition: all 0.3s;
    }
  }
}
.select_wrap.active .default_option .chevron {
  transform: rotate(-225deg);
}

.select_wrap .select_ul {
  position: absolute;
  top: 60px;
  left: 0;
  width: 100%;
  background: #fff;
  z-index: 1;
  display: none;
}

.select_wrap .select_ul li {
  padding: 20px 16px;
  cursor: pointer;
  &:hover {
    background: #fbfbfb;
  }
  p {
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
}

.select_wrap .option {
  display: flex;
  align-items: center;
}

.select_wrap.active .select_ul {
  display: block;
}
</style>
