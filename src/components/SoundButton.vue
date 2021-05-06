<template>
  <button @click="playItAgainSam" :style="backgroundColor">
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: {
    audio: String,
  },
  data() {
    return {
      audioFile: "",
      backgroundColor: "background-color: #" + ((Math.random() * 0xffffff) << 0).toString(16),
    };
  },
  methods: {
    playItAgainSam() {
      console.log("ive been clicked->", this.audio);

      try {
        this.audioFile.play();
      } catch (e) {
        console.log(e);
      }
    },
  },
  mounted() {
    console.log("Props are loaded->", this.audio);

    // requires is needed. Else it's a string.
    // https://stackoverflow.com/a/51126831/4096078

    this.audioFile = new Audio(require("../assets/" + this.audio + ".wav"));
  },
};
</script>

<style>
</style>