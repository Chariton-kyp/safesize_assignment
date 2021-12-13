<template>
  <div class="filter_button_container ps-0 ms-0 mt-1 d-flex">
    <button class="filter_button btn">Remove all</button>
    <button :class="{active: colored}" class="filter_button btn">Apply</button>
  </div>
</template>

<script>
export default {
  name: "FilterButtons",
  data(){
      return{
          colored: true,
      }
  }
};
</script>

<style scoped lang="scss">
.filter_button {
  width: 215px;
  height: 72px;
  margin: 12px 12px 0 0;
  padding: 18px 26.7px 23px 26.7px;
  background-color: #fff;
  box-shadow: 1px 1px 2px 0 rgba(0, 0, 0, 0.18),
    0 1.1px 5px 0 rgba(0, 0, 0, 0.2);
  background-color: #fff;
  border-radius: 15px;
  font-size: 24px;
  font-weight: bold;
  color: #006eb7;
}
.filter_button_container {
  width: 453px;
  height: 100px;
  flex-grow: 0;
  margin: 0 0 0 12px;
  padding: 2px 0 20px;
  background-color: #fff;
}
.active{
    background-color: #006eb7;
    color: #fff;
    font-size: 24px;
}

@media (max-width: 767.98px) {
  .filter_button {
    width: 137px;
    height: 54px;
    margin: 0 21px 0 0;
    padding: 15px 2.1px 15px 2px;
    box-shadow: 1px 1px 2px 0 rgba(0, 0, 0, 0.18),
      0 1.1px 5px 0 rgba(0, 0, 0, 0.2);
    background-color: #fff;
      font-size: 16px;
  font-weight: bold;
  color: #006eb7;
  }
  .filter_button_container {
    width: 319px;
    height: 81px;
    flex-grow: 0;
    padding: 8px 0px 2px 12px;
    background-color: #fff;
  }
  .active{
    background-color: #006eb7;
    color: #fff;
}
}
</style>
