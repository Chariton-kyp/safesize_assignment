<template>
  <nav class="custom_navbar navbar navbar-expand-lg navbar-toggler bg-white">
    <div class="container-fluid ps-0">
      <div class="ms-2 ps-3 d-none d-md-block">
        <a class="navbar-brand main_nav" href="#"
          ><img
            alt="Safesize logo"
            src="../assets/safesize_logo.png"
            width="100"
            height="62.8"
        /></a>
      </div>
      <div class="d-md-none d-flex secondary_nav">
        <button
          v-if="filtersMobile"
          @click="toggleFilters()"
          class="btn shadow-none ps-0"
        >
          <span>
            <img
              class="x_button"
              src="../assets/x_image_md.png"
              alt="an X image to close filters"
          /></span>
        </button>
        <div v-if="!filtersMobile">
          <button
            @click="toggleFilters()"
            class="btn shadow-none ps-0"
            href="#"
          >
            <span>
              <img class="me-3" alt="Filters" src="../assets/filter.png"
            /></span>
          </button>
          <b>FILTERS</b>
        </div>
      </div>
      <Cart class="d-md-none d-inline"></Cart>
      <Cart class="d-none d-md-flex"></Cart>
    </div>
  </nav>
  <p v-if="!filtersMobile" class="ms-3 mb-auto fs-5 d-flex d-md-none mb-0">
    Our recommendation
  </p>
  <div v-if="filtersMobile" class="background_filter d-flex d-md-none">
    <div
      class="filter_container_mobile d-flex flex-column ms-auto d-md-none position-relative overflow-hidden"
    >
      <FunctionalAdvice></FunctionalAdvice>
      <SearchForm></SearchForm>
      <hr class="hrs" />
      <span class="custom_Filters mt-3">Filters</span>
      <ul class="ps-0">
        <li class="list-group">
          <Brand></Brand>
          <hr class="hrs" />
        </li>
        <li class="list-group">
          <Colours></Colours>
          <hr class="hrs" />
        </li>
        <li class="list-group">
          <Gender></Gender>
          <hr class="hrs" />
        </li>
        <li class="list-group">
          <Fabric></Fabric>
          <hr class="hrs" />
        </li>
        <div class="mt-1">
          <span class="span_nav">Availability • </span>
          <span class="custom_selected ms-1 mb-0"> 1 selected</span>
        </div>
      </ul>

      <div class="filter_button position-absolute">
        <FilterButtons></FilterButtons>
      </div>
    </div>
  </div>
</template>

<script>
import FunctionalAdvice from "@/components/FunctionalAdvice.vue";
import SearchForm from "@/components/SearchForm.vue";
import Cart from "@/components/Cart.vue";
import Brand from "@/components/Brand.vue";
import Colours from "@/components/Colours.vue";
import Gender from "@/components/Gender.vue";
import Fabric from "@/components/Fabric.vue";
import FilterButtons from "@/components/FilterButtons.vue";

export default {
  name: "NavBar",
  data() {
    return {
      filtersMobile: false,
    };
  },
  components: {
    Cart,
    FunctionalAdvice,
    SearchForm,
    Brand,
    Colours,
    Gender,
    Fabric,
    FilterButtons,
  },
  methods: {
    toggleFilters() {
      this.filtersMobile = !this.filtersMobile;
    },
  },
};
</script>

<style scoped lang="scss">
.secondary_nav {
  font-size: 12px;
  height: 42px;
  align-items: center;
}
.main_nav {
  height: 72px;
}
.filter_container_mobile {
  margin-top: -33px;
  padding: 18px 12px 0px;
  width: 319px;
  height: 640px;
  box-shadow: 0 6px 37px 0 rgba(0, 0, 0, 0.22);
  background-color: #fff;
}
.hrs {
  margin: 0 0;
  height: 2px;
  border-top: 1px solid #e7e7e7;
}
.x_button {
  width: 13px;
  height: 13px;
}
.background_filter {
  width: 100%;
  height: 607.202px;
  margin: -20px 0.5px 0 0;
  padding: 0 0 587px;
  background-color: rgba(64, 64, 64, 0.5);
}
.custom_Filters {
  font-weight: 500;
  font-size: 14px;
}
.span_nav {
  font-weight: 500;
}
.custom_selected {
  font-size: 16px;
  font-weight: 500;
  color: #006eb7;
  letter-spacing: 0.5px;
}


@media (max-width: 767.98px) {
  .custom_navbar {
    border-radius: 0 0 20px 20px;
    box-shadow: 0 2px 20px 0 rgba(64, 64, 64, 0.11);
  }
  .span_nav {
    font-size: 12px;
    font-weight: 500;
  }
  .custom_selected {
    font-size: 12px;
    font-weight: 500;
    color: #006eb7;
    letter-spacing: 0.5px;
  }
  .filter_button {
    width: 319px;
  height: 81px;
  margin: 540px 0 0;
  background-color: #fff;
}
}

</style>
