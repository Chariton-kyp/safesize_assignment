<template>
  <NavBar></NavBar>
  <div class="d-flex">
    <Filters ></Filters>
    
    <div class="mobile_breakpoint d-flex d-md-none">
      <div>
        <div class="ms-2 ps-1">
          <div class="row d-flex">
            <ul class=" col-md-6 col-sm-12 list-group" v-for="n in 15" :key="n">
              <li class="list-group mt-2 mb-3" >
                <Products class=""></Products>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div class="desktop_breakpoint d-none d-md-flex ">
      <div class="my-4">
        <span></span>
        <span class="span-class ps-2 position-absolute">15 RESULTS</span>
      </div>
      <div>
        <div class="ms-2 ps-6">
          <div class="row d-flex">
            <ul class="col-xxl-4 col-xl-6 col-md-12 mt-4 pt-4 list-group" v-for="n in 15" :key="n">
              <li class="list-group mt-2 mb-3" >
                <Products class=""></Products>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from "@/components/NavBar.vue";
import Filters from "@/components/Filters.vue";
import Products from "@/components/Products.vue";

export default {
  name: "Home",
  components: {
    NavBar,
    Filters,
    Products,
  },
  data() {
    return {
      Products,
    };
  },
};
</script>
<style scoped lang="scss">
.desktop_breakpoint div span {
  margin-left: 12px;
  padding-left: 480px ;

}
.span_class{
  font-size: 20px;
  font-weight: 500;
  margin: 15px 500px 10px 0;
  padding-left: 12px;
}
</style>
