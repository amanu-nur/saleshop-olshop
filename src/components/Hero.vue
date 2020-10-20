<template>
  <div class="jumbotron jumbotron-fluid">
    <div class="container">
      <div class="row">
        <div class="col-lg">
          <h1 class="h2 text-hero ">
            Hard To Find Items, <br />
            We Have A Solution For You
          </h1>
          <p class="promotion ">
            We provide what you need, the convenience of family shopping. It's
            time to make family shopping moments memorable.
          </p>
          <button type="button" class="btn btn-warning text-white ">
            Show Me Now
          </button>
        </div>
        <div class="col-lg">
          <Lottie id="lottie-hero" :options="defaultOptions" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Lottie from "../../node_modules/vue-lottie/src/lottie.vue";
import animationData from "../../public/Animations/hero.json";

export default {
  components: {
    Lottie,
  },
  name: "Hero",
  data() {
    return {
      defaultOptions: { animationData: animationData },
      animationSpeed: 1.5,
    };
  },
};
</script>
