<template>
  <!-- mobile breakpoint -->
  <div class="d-inline d-md-none position-relative">
    <div class="justify-content-between d-flex bg-white">
      <p class="advice_sm pt-0 pb-0 mb-0">{{ advice }}</p>
      <button class="button_advice btn mb-auto pt-0 py-0 shadow-none">
        <img
          class="active_button"
          alt="active button image"
          src="../assets/Active.png"
        />
      </button>
    </div>
    <ul class="before_categories list-group">
      <li
        class="categories_mobile d-flex justify-content-between"
        v-for="item in categories"
        :key="item"
      >
        {{ item }}
        <img
          class="info_icon"
          src="../assets/icon-info-mobile.png"
          alt="info image"
        />
      </li>
    </ul>
  </div>
  <!-- desktop breakpoint-->
  <div class="functional_box d-none d-md-block">
    <div class="justify-content-between d-none d-md-flex">
      <p class="d-none d-md-flex mb-0">{{ advice }}</p>
      <button class="btn mb-auto p-0 shadow-none">
        <img 
        alt="active button image" 
        src="../assets/Active.png" 
        />
      </button>
    </div>
    <ul class="before_categories list-group">
      <li
        class="categories d-flex justify-content-between"
        v-for="item in categories"
        :key="item"
      >
        {{ item }} <img src="../assets/icon-info.png" alt="info image" />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "FunctionalAdvice",
  data() {
    return {
      advice: "Functional advice",
      categories: {
        category: "CATEGORY: ROAD",
        cushioning: "CUSHIONING: CUSHIONING",
        stability: "STABILITY: STABLE +",
      },
    };
  },
};
</script>

<style scoped lang="scss">
.advice_sm {
  font-size: 14px;
  font-weight: 500;
}
.filter_mobile {
  position: relative;
}
.functional_box {
  margin: 0 12px;
}
.active_button {
  width: 46px;
  height: 22px;
}
.before_categories {
  margin-top: 30px;
}
.categories {
  background-color: #d8edf8;
  border-radius: 6.3px;
  padding: 8px 15px 7px;
  margin-bottom: 11px;
  font-weight: 500;
  letter-spacing: 0.5px;
  color: #006eb7;
}
.categories_mobile {
  background-color: #d8edf8;
  border-radius: 6.3px;
  padding: 7px 17px 8px;
  margin-bottom: 10px;
  font-weight: 500;
  letter-spacing: 0.5px;
  color: #006eb7;
  font-size: 12px;
}
.info_icon {
  width: 16px;
  height: 16px;
}
.button_advice{
  margin-top: -5px;
}
</style>
