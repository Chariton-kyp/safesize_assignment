<template>
  <!-- container for the filter container - desktop breakpoint -->
      <button v-if="!filtersMobile" @click="toggleFilters()"
      class="d-none d-md-flex mx-0 btn shadow-none"><img
        class="right_arrow"
        alt="right arrow image"
        src="../assets/right_arrow.png"
      />
    </button>
  <div v-if="filtersMobile"
    class="filter_container_desk d-none d-md-inline-block bg-white position-absolute"
  >
    <!-- div for the recommendation -->
    <button
      v-if="filtersMobile"
      @click="toggleFilters()"
      class="d-none d-md-flex mx-0 btn shadow-none"
    >
      <img
        class="left_arrow"
        alt="left arrow image"
        src="../assets/left_arrow.png"
      />
      <span class="recom ms-3">Our recommendations</span>
    </button>

    <FunctionalAdvice></FunctionalAdvice>
    <SearchForm class="ms-auto mt-4 pb-0 d-none d-md-flex"></SearchForm>
    <hr class="hrs" />
    <div class="mt-5 ms-2 ps-1">
      <span class="span_filters fs-5">Filters</span>
      <Brand></Brand>
    </div>
    <hr class="hrs" />
    <div class="mt-3 mb-1 ms-2 ps-1">
      <Colours></Colours>
    </div>
    <hr class="hrs" />
    <div class="mt-3 mb-1 ms-2 ps-1">
      <Gender></Gender>
    </div>
    <hr class="hrs" />
    <div class="mt-3 mb-1 ms-2 ps-1">
      <Fabric></Fabric>
    </div>
    <hr class="hrs" />
    <div class="ms-2 ps-1 mt-3">
      <span class="span_filters">Availability • </span>
      <span class="custom_selected"> 1 selected</span>
    </div>
    <div class="position-absolute ms-2 ps-1">
      <FilterButtons></FilterButtons>
    </div>
  </div>
</template>

<script>
import FunctionalAdvice from "@/components/FunctionalAdvice.vue";
import SearchForm from "@/components/SearchForm.vue";
import Brand from "@/components/Brand.vue";
import Colours from "@/components/Colours.vue";
import Gender from "@/components/Gender.vue";
import Fabric from "@/components/Fabric.vue";
import FilterButtons from "@/components/FilterButtons.vue";

export default {
  name: "Filters",
    data() {
    return {
      filtersMobile: true,
    };
  },
  components: {
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
.left_arrow {
  width: 15px;
  height: 23px;
  margin-top: 10px;
}
.filter_container_desk {
  width: 480px;
  height: 1200px;
  margin-left: 12px;
}
.recom {
  letter-spacing: 0.3px;
  font-size: 32px;
  font-weight: 500;
}
.span_fabric {
  font-weight: 500;
}
.hrs {
  margin: 0px 11px 0;
  height: 2px;
  border-top: 1px solid #e7e7e7;
}
.brand {
}
.span_filters {
  font-weight: 500;
}
.custom_selected {
  font-size: 16px;
  font-weight: 500;
  color: #006eb7;
  letter-spacing: 0.5px;
}
@media (max-width: 767.98px) {
  .span_fabric {
    font-size: 12px;
    font-weight: 500;
  }
  .custom_selected {
    font-size: 16px;
    font-weight: 500;
    color: #006eb7;
    letter-spacing: 0.5px;
  }
}
</style>
