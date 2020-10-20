<template>
  <div class="success">
    <div class="container">
      <div class="row">
        <div class="col">
          <h2 class="text-congrats">
            Yeay, Pesanan Anda Telah Kami Terima
          </h2>
          <h3 class="message">
            Product Akan Segera Kami Proses Dan Tunggu Informasi <br />
            Terbaru Dari Kami Via Email
          </h3>
          <div class="col-lg background-animation">
            <Lottie id="lottie-success" :options="defaultOptions" />
          </div>
          <router-link class="btn btn-warning text-white" to="/"
            >Back To Home</router-link
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Lottie from "../../node_modules/vue-lottie/src/lottie.vue";
import animationData from "../../public/Animations/success.json";

export default {
  components: {
    Lottie,
  },
  name: "Home",
  data() {
    return {
      defaultOptions: { animationData: animationData },
      animationSpeed: 1.5,
    };
  },
};

window.scrollTo(0, 0);
</script>
