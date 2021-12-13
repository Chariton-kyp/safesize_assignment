b
<template>
  <div class="d-flex justify-content-between ms-0 ps-0">
    <div class="mb-2">
      <span class="span_colour ms-0 ps-0">Colour</span>
    </div>
    <div class="">
      <button class="arrow_up_btn d-flex btn shadow-none rounded pt-0 mt-2">
        <img
          @click="toggleColour()"
          v-if="colourOpen"
          class="arrow_up"
          src="../assets/arrow_up.png"
          alt="arrow up button for opening brand filter"
        />
        <img
          @click="toggleColour()"
          v-if="!colourOpen"
          class="arrow_up"
          src="../assets/arrow_down.png"
          alt="arrow up button for opening brand filter"
        />
      </button>
    </div>
  </div>
  <div v-if="colourOpen" class="container ps-0">
    <div class="row">
      <div class="col-3">
        <button
          class="custom_button shadow-none"
          :class="{ active: whiteSelected }"
          @click="buttonSelected('White')"
        >
          White
        </button>
      </div>
      <div class="col-3">
        <button
          class="custom_button shadow-none"
          :class="{ active: blackSelected }"
          @click="buttonSelected('Black')"
        >
          Black
        </button>
      </div>
      <div class="col-3">
        <button
          class="custom_button shadow-none"
          :class="{ active: blueSelected }"
          @click="buttonSelected('Blue')"
        >
          Blue
        </button>
      </div>
      <div class="col-3">
        <button
          class="custom_button shadow-none"
          :class="{ active: greySelected }"
          @click="buttonSelected('Grey')"
        >
          Grey
        </button>
      </div>
      <div class="col-3">
        <button
          class="custom_button shadow-none"
          :class="{ active: purpleSelected }"
          @click="buttonSelected('Purple')"
        >
          Purple
        </button>
      </div>
      <div class="col-3">
        <button
          class="custom_button shadow-none"
          :class="{ active: greenSelected }"
          @click="buttonSelected('Green')"
        >
          Green
        </button>
      </div>
      <div class="col-3">
        <button
          class="custom_button shadow-none"
          :class="{ active: brownSelected }"
          @click="buttonSelected('Brown')"
        >
          Brown
        </button>
      </div>
      <div class="col-3">
        <button
          class="custom_button shadow-none"
          :class="{ active: redSelected }"
          @click="buttonSelected('Red')"
        >
          Red
        </button>
      </div>
      <div class="col-3">
        <button
          class="custom_button shadow-none"
          :class="{ active: pinkSelected }"
          @click="buttonSelected('Pink')"
        >
          Pink
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Colours",
  data() {
    return {
      whiteSelected: false,
      blackSelected: false,
      blueSelected: false,
      greySelected: false,
      purpleSelected: false,
      greenSelected: false,
      brownSelected: false,
      redSelected: false,
      pinkSelected: false,
      colourOpen:false,
    };
  },
  methods: {
    buttonSelected(colour) {
      if (colour === "White") {
        this.whiteSelected = !this.whiteSelected;
      } else if (colour === "Black") {
        this.blackSelected = !this.blackSelected;
      } else if (colour === "Blue") {
        this.blueSelected = !this.blueSelected;
      } else if (colour === "Grey") {
        this.greySelected = !this.greySelected;
      } else if (colour === "Purple") {
        this.purpleSelected = !this.purpleSelected;
      } else if (colour === "Green") {
        this.greenSelected = !this.greenSelected;
      } else if (colour === "Brown") {
        this.brownSelected = !this.brownSelected;
      } else if (colour === "Red") {
        this.redSelected = !this.redSelected;
      } else if (colour === "Pink") {
        this.pinkSelected = !this.pinkSelected;
      }
    },
    toggleColour() {
      this.colourOpen = !this.colourOpen;
    },
  },
};
</script>

<style scoped lang="scss">
.custom_button {
  width: 101px;
  height: 55px;
  flex-grow: 0;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 10px;
  margin: 0 12px 15px 0;
  padding: 10px 16px;
  border-radius: 15px;
  box-shadow: 0 3px 3px 0 rgba(0, 0, 0, 0.16);
  border: solid 1px rgba(145, 150, 152, 0.6);
  background-color: #fff;
  color: #919698;
  font-weight: bold;
  font-size: 20px;
}
.active {
  background-color: #006eb7;
  color: #ffffff;
}
.span_colour {
  font-weight: 500;
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
  margin-right: 12px;
  padding: 0;
}
@media (max-width: 767.98px) {
  .custom_button {
    font-size: 14px;
    font-weight: bold;
    width: 59px;
    height: 59px;
    color: #919698;
    border-radius: 15px;
    box-shadow: 0 3px 3px 0 rgba(0, 0, 0, 0.16);
    border: solid 1px rgba(145, 150, 152, 0.6);
  }
  .active {
    background-color: #006eb7;
    color: #ffffff;
  }
  .span_colour {
    font-size: 12px;
    font-weight: 500;
  }
    .arrow_up_btn{
      margin-right: 0px;
  } 
}
</style>
