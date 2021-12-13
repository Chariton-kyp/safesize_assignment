<template>
  <div class="d-flex justify-content-right">
    <p class="mt-3 me-3 fw-bold d-none d-md-inline">{{ name }}</p>
    <div class="ellipse">
      <div class="position-absolute small_ellipse">
        <span class="d-none d-md-flex fs-6 fw-bold">0</span>
        <span class="d-flex d-md-none fw-bold zero_letter">0</span>
      </div>
      <a href="#"><img
        class="position-absolute shoe"
        alt="shoe image"
        src="../assets/shoe.png"
      /></a>
    </div>

    <div class="profile">
      <a href="#"><p class="mt-2 ms-1 fw-bold d-flex d-md-none fs-6">{{ small_name }}</p></a>
      <div class="opacity-1">
        <a href="#"
          ><img
            class="mt-3 ms-3 d-none d-md-flex position-absolute"
            alt="dropdown icon"
            src="../assets/dropdown_icon.png"
        /></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Cart",
  data() {
    return {
      name: "Aristotelis Michailidis",
    };
  },
  computed: {
    small_name: function () {
      let splited_name = this.name.split(" ");
      let letters = splited_name[0][0] + splited_name[1][0];
      return letters;
    },
  },
};
</script>

<style lang="scss">
@media (max-width: 767.98px) {
    .profile a{
        text-decoration: none;
    }
  .profile {
    width: 35px;
    height: 35px;
    box-shadow: 1px 1px 3px 0 rgba(64, 64, 64, 0.25);
    background-color: #fff;
    border-radius: 45px;
    margin: 0 0 0 20px;
  }
  .small_ellipse {
    width: 17px;
    height: 17px;
    flex-grow: 0;
    padding: 2px 5px 1px;
    margin: -4px 0 0 -4px;
    border: solid 1px #3ea3dc;
    background-color: #fff;
    border-radius: 45px;
  }
  .ellipse {
    width: 35px;
    height: 35px;
    flex-grow: 0;
    margin: 0;
    padding: 0 20px 0 0;
    background-color: #3ea3dc;
    border-radius: 45px;
  }
  .shoe {
    width: 22.5px;
    height: 10.5px;
    margin: 12px 6px;
  }
  .zero_letter {
    margin: 0 0 0 -1px;
    font-size: 12px;
  }
}
@media (min-width: 767.99px) {
  .profile {
    width: 55px;
    height: 55px;
    flex-grow: 0;
    margin: 0 0 0 20px;
    background-color: #e9e7e7;
    border-radius: 45px;
  }
  .small_ellipse {
    width: 25px;
    height: 25px;
    flex-grow: 0;
    margin: -5px 37px 36.3px -6px;
    padding: 2px 7.5px 1.6px 8px;
    border: solid 1px #3ea3dc;
    background-color: #fff;
    border-radius: 45px;
  }
  .ellipse {
    width: 55px;
    height: 55px;
    flex-grow: 0;
    margin: 0 0 0 7px;
    background-color: #3ea3dc;
    border-radius: 45px;
  }
  .shoe {
    width: 35.4px;
    height: 16.5px;
    margin: 19px 10px;
  }
}
</style>
