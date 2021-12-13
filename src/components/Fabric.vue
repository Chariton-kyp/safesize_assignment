<template>
  <div class="d-flex justify-content-between ms-0 ps-0">
    <div class="mb-2">
      <span class="span_fabric ms-0 ps-0">Fabric</span>
    </div>
    <div class="">
      <button class="arrow_up_btn d-flex btn shadow-none rounded pt-0 mt-2">
        <img
          @click="toggleFabric()"
          v-if="fabricOpen"
          class="arrow_up"
          src="../assets/arrow_up.png"
          alt="arrow up button for opening brand filter"
        />
        <img
          @click="toggleFabric()"
          v-if="!fabricOpen"
          class="arrow_up"
          src="../assets/arrow_down.png"
          alt="arrow up button for opening brand filter"
        />
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fabricOpen: false,
    };
  },
  name: "Fabric",
  methods: {
    toggleFabric() {
      this.fabricOpen = !this.fabricOpen;
    },
  },
};
</script>

<style scoped lang="scss">
.arrow_up {
  width: 15px;
  height: 10px;
  border: none;
}
.span_fabric {
  font-weight: 500;
}
.arrow_up_btn {
  width: 15;
  height: 10px;
  border: none;
  margin-right: 12px;
  padding: 0;
}
@media (max-width: 767.98px) {
      .span_fabric {
    font-size: 12px;
    font-weight: 500;
  }
    .arrow_up_btn{
      margin-right: 0px;
  } 
}
</style>