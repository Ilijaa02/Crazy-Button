<template>
  <div id="app">
    <button
      :style="{
        border: border1,
        borderRadius: borderRadius1,
        color: color1,
        width: width1,
        height: height1,
      }"
      @click="changeButton"
    >
      Click me
    </button>
  </div>
</template>

<script>
export default {
  name: "Button",
  data() {
    return {
      border1: "",
      borderRadius1: "",
      color1: "",
      width1: "",
      height1: "",
      borderStyle: [
        "dotted",
        "dashed",
        "solid",
        "double",
        "groove",
        "ridge",
        "inset",
        "outset",
      ],
    };
  },
  methods: {
    changeButton() {
      let borderStyleIndex = Math.floor(Math.random() * 7) + 1;
      this.border1 = `${Math.floor(Math.random() * 12) + 3}px ${
        this.borderStyle[borderStyleIndex]
      } #${Math.floor(Math.random() * 9) + 1}${
        Math.floor(Math.random() * 9) + 1
      }${Math.floor(Math.random() * 9) + 1}${
        Math.floor(Math.random() * 9) + 1
      }${Math.floor(Math.random() * 9) + 1}${
        Math.floor(Math.random() * 9) + 1
      }`;
      this.borderRadius1 = `${Math.floor(Math.random() * 45) + 10}px`;
      this.color1 = `#${Math.floor(Math.random() * 9) + 1}${
        Math.floor(Math.random() * 9) + 1
      }${Math.floor(Math.random() * 9) + 1}${
        Math.floor(Math.random() * 9) + 1
      }${Math.floor(Math.random() * 9) + 1}${
        Math.floor(Math.random() * 9) + 1
      }`;
      this.width1 = `${Math.floor(Math.random() * 400) + 100}px`;
      this.height1 = `${Math.floor(Math.random() * 100) + 40}px`;
    },
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  display: flex;
  align-items: center;
  flex-direction: column;
}
button {
  font-size: 23px;
  margin-top: 50px;
  cursor: pointer;
  background-color: white;
  min-height: 50px !important;
}
</style>