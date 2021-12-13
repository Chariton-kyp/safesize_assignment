<template>
  <div class="custom_brand d-flex justify-content-between mt-3 pb-2">
    <div class="d-inline">
      <span class="mb-1">Brand •</span>
      <span class="custom_selected ms-1 mb-0">{{ counter }} selected</span>
    </div>
    <div>
      <button class="arrow_up_btn d-flex btn shadow-none rounded pt-0 mt-0">
        <img
          @click="toggleBrand()"
          v-if="brandOpen"
          class="arrow_up"
          src="../assets/arrow_up.png"
          alt="arrow up button for opening brand filter"
        />
        <img
          @click="toggleBrand()"
          v-if="!brandOpen"
          class="arrow_up"
          src="../assets/arrow_down.png"
          alt="arrow up button for opening brand filter"
        />
      </button>
    </div>
  </div>
  <ul v-if="brandOpen" class="ps-0">
    <li class="list-group custom_list">
      <div class="form-check checkboxes">
        <input
          class="custom_checkbox form-check-input shadow-none rounded-circle"
          type="checkbox"
          value="1"
          v-model="checkedNumbers"
          id="flexCheckDefault"
        />
        <label class="custom_li form-check-label" for="flexCheckDefault"
          >{{ brands[0] }}
        </label>
      </div>
    </li>
    <li class="list-group custom_list">
      <div class="form-check checkboxes">
        <input
          class="custom_checkbox form-check-input shadow-none rounded-circle"
          type="checkbox"
          value="10"
          v-model="checkedNumbers"
          id="flexCheckDefault1"
        />
        <label class="custom_li form-check-label" for="flexCheckDefault1"
          >{{ brands[1] }}
        </label>
      </div>
    </li>
    <li class="list-group custom_list">
      <div class="form-check checkboxes">
        <input
          class="custom_checkbox form-check-input shadow-none rounded-circle"
          type="checkbox"
          value="100"
          v-model="checkedNumbers"
          id="flexCheckDefault2"
        />
        <label class="custom_li form-check-label" for="flexCheckDefault2"
          >{{ brands[2] }}
        </label>
      </div>
    </li>
    <li class="list-group custom_list">
      <div class="form-check checkboxes">
        <input
          class="custom_checkbox form-check-input shadow-none rounded-circle"
          type="checkbox"
          value="1000"
          v-model="checkedNumbers"
          id="flexCheckDefault3"
        />
        <label class="custom_li form-check-label" for="flexCheckDefault3"
          >{{ brands[3] }}
        </label>
      </div>
    </li>
    <li class="list-group custom_list">
      <div class="form-check checkboxes">
        <input
          class="custom_checkbox form-check-input shadow-none rounded-circle"
          type="checkbox"
          value="10000"
          v-model="checkedNumbers"
          id="flexCheckDefault4"
        />
        <label class="custom_li form-check-label" for="flexCheckDefault4"
          >{{ brands[4] }}
        </label>
      </div>
    </li>
    <li class="list-group custom_list">
      <div class="form-check checkboxes">
        <input
          class="custom_checkbox form-check-input shadow-none rounded-circle"
          type="checkbox"
          value="100000"
          v-model="checkedNumbers"
          id="flexCheckDefault5"
        />
        <label class="custom_li form-check-label" for="flexCheckDefault5"
          >{{ brands[5] }}
        </label>
      </div>
    </li>
    <li class="list-group custom_list">
      <div class="form-check checkboxes">
        <input
          class="custom_checkbox form-check-input shadow-none rounded-circle"
          type="checkbox"
          value="1000000"
          v-model="checkedNumbers"
          id="flexCheckDefault6"
        />
        <label class="custom_li form-check-label" for="flexCheckDefault6"
          >{{ brands[6] }}
        </label>
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  name: "Brand",
  data() {
    return {
      brands: [
        "New Balance",
        "Adidas",
        "Nike Performance",
        "Reebok",
        "Asics",
        "Under Armour",
        "Puma",
      ],
      checkedNumbers: [],
      brandOpen: true,
    };
  },
  methods: {
    toggleBrand() {
      this.brandOpen = !this.brandOpen;
    },
  },
  computed: {
    sum() {
      return this.checkedNumbers.reduce(function (a, b) {
        return parseInt(a) + parseInt(b);
      }, 0);
    },
    counter() {
      let num = this.sum;
      let digits = num.toString().split("");
      let realDigits = digits.map(Number);
      let counting = 0;
      for (const item of realDigits) {
        if (item == 1) {
          counting = counting + 1;
        }
      }
      return counting;
    },
  },
};
</script>

<style scoped lang="scss">
.custom_brand {
  font-weight: 500;
  font-size: 12px;
}
.custom_list {
  font-size: 10px;
  font-weight: 500;
  margin-top: -4px;
}
.custom_selected {
  font-size: 12px;
  font-weight: 500;
  color: #006eb7;
  letter-spacing: 0.5px;
}
.arrow_up {
  width: 15px;
  height: 10px;
  border: none;
}
.arrow_up_btn {
  width: 15;
  height: 10px;
  border: none;
  margin: 0;
  padding: 0;
}
@media (min-width: 767.98px) {
  .custom_brand {
    font-size: 16px;
  }
  .custom_selected {
    font-size: 16px;
    font-weight: 500;
    color: #006eb7;
    letter-spacing: 0.5px;
  }
  .custom_li {
    font-size: 14px;
    font-weight: normal;
  }
  .custom_checkbox {
    width: 18px;
    height: 18px;
    margin: 0 16px 13px 0;
  }
  .checkboxes {
    padding: 0;
  }
  .arrow_up_btn{
      margin-right: 10px;
  } 
}
</style>
