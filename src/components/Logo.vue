<template>
   <div class="logo-container">
      <img
        class="logo-image"
        alt="logo"
        src="../assets/slotted-glasses.png"
        width="400"
        :style="imageFilter"
      />
      <div class="logo-text">DJ VUE</div>
    </div>
</template>

<script>
export default {
  data() {
    return {
    randomDegree: 0,
    imageFilter: "",
    };
  },
  mounted() {
    this.randomDegree = Math.floor(Math.random() * 178) + 1;
    this.imageFilter = "filter: hue-rotate(" + this.randomDegree + "deg);";
  }
}
</script>

<style>


.logo-container {
  position: relative;
  text-align: center;
  color: white;
}

.logo-image {
  width: 100%;
  margin-bottom: 20px;
}

.logo-text {
  font-size: clamp(4rem, 15vw + 8.333vw, 10rem);
  color: blue;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>