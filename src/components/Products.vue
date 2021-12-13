<template>
  <div class="shoe_container container d-flex position-relative bg-white">
    <div class="m-auto">
      <a href="#"><img class="nike" src="../assets/nike.png" alt="nike shoe image" /></a>
    </div>
    <div class="name_position position-absolute">
      <p>{{ name }}</p>
    </div>
    <div class="discount position-absolute">
      <img src="../assets/discount_label.png" alt="discount label image" />
      <span class="span_discount">99%</span>
    </div>
    <div class="store_class d-flex position-absolute">
      <div class="d-flex">
        <img
          class="online"
          src="../assets/online_store.png"
          alt="online image"
        />
        <span class="online_span">Online</span>
      </div>
      <div class="d-flex">
        <img class="store" src="../assets/in_store.png" alt="store image" />
        <span class="store_span">In-store</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Products",
  data() {
    return {
      name: "Nike Free Run",
    };
  },
};
</script>

<style scoped lang="scss">
.nike {
  width: 250px;
  height: 250px;
}
.shoe_container {
  width: 400px;
  height: 295px;
  border-radius: 15px;
}
.name_position {
  width: 400px;
  height: 45px;
  margin: 227px 100px 23px;
  font-size: 24px;
  font-weight: 500;
}
.discount img {
  margin-left: -30px;
  margin-top: -10px;
  width: 90px;
}
.span_discount {
  margin-left: -65px;
  font-size: 24px;
  font-weight: bold;
  color: #fff;
}
.online {
  width: 25px;
  height: 25px;
  margin-right: 8px;
}
.store {
  width: 25px;
  height: 25px;
  margin-right: 8px;
}
.store_class {
  margin-left: 180px;
  margin-top: 20px;
}
.store_class div {
  margin: 0 10px;
  font-size: 14px;
}
.online_span{
    color: #3ea3dc;
    font-weight: 500;
}
.store_span{
    color: #27ae60;
    font-weight: 500;
}
@media (max-width:767.98px){
    .nike {
  width: 220px;
  height: 220px;
}
.shoe_container {
  width: 336px;
  height: 220px;
  border-radius: 15px;
}
.name_position {
  width: 444px;
  height: 45px;
  margin: 180px 80px 0px;
  font-size: 24px;
  font-weight: 500;
}
.discount img {
  margin-left: -18px;
  margin-top: -8px;
  width: 65px;
}
.span_discount {
  margin-left: -50px;
  font-size: 16px;
  font-weight: bold;
  color: #fff;
}
.online {
  width: 15px;
  height: 15px;
  margin-right: 6px;
}
.store {
  width: 15px;
  height: 15px;
  margin-right: 6px;
}
.store_class {
  margin-left: 180px;
  margin-top: 15px;
}
.store_class div {
  margin: 0 5px;
  font-size: 10px;
}
.online_span{
    color: #3ea3dc;
    font-weight: 500;
}
.store_span{
    color: #27ae60;
    font-weight: 500;
}
}
</style>
