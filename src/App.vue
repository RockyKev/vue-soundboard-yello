<template>
  <div id="app">
    <!-- <div class="logo-container">
      <img
        class="logo-image"
        alt="logo"
        src="./assets/slotted-glasses.png"
        width="400"
      />
      <div class="logo-text">DJ VUE</div>
    </div> -->
    <Logo />

    <div class="button-set">
      <sound-button audio="oh-yeah">OOOH YEAH!</sound-button>
      <sound-button audio="ouch-ouch">AUCH AUCH</sound-button>
      <sound-button audio="the-moon">The MOOOOON!</sound-button>
      <sound-button audio="beautiful">BEAUTIFUL</sound-button>
      <sound-button audio="even-more-beautiful"
        >Even More Beautiful</sound-button
      >
      <sound-button audio="chicka-chicka">CHICKA CHICKA</sound-button>
    </div>

    <Footer />
  </div>
</template>

<script>
import Logo from "./components/Logo.vue";
import SoundButton from "./components/SoundButton.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Logo,
    SoundButton,
    Footer,
  },
  data() {
    return {
      buttonCollection: [],
    };
  },
};
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
}

.button-set {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

button {
  /* https://css-tricks.com/adding-stroke-to-web-text/ */

  background-color: pink;
  text-transform: uppercase;
  font-size: 2rem;
  font-weight: 900;
  width: 100%;
  padding: 40px;
  margin: 10px 20px;
  -webkit-text-fill-color: white;
  -webkit-text-stroke-width: 2px;
  -webkit-text-stroke-color: black;
}

@media only screen and (min-width: 600px) {
  button {
    width: 40%;
  }
}

</style>
