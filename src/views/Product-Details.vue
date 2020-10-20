<template>
  <div class="Product-Details">
    <Navbar />

    <!-- Breadcurmb -->

    <nav aria-label="breadcrumb">
      <div class="container">
        <ol class="breadcrumb">
          <li class="breadcrumb-item">
            <router-link to="/"><i class="fas fa-home"></i> Home</router-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">Details</li>
        </ol>
      </div>
    </nav>

    <!-- End -->
    <!-- Details -->

    <div class="product-shop spad page-details">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="row">
              <div class="col-lg-6">
                <div class="product-pic">
                  <img class="product-big" :src="gambar_default" alt="" />
                </div>
                <div class="product-thumbs">
                  <carousel
                    class="product-thumbs-track ps-slider"
                    :nav="false"
                    :dots="false"
                  >
                    <div
                      class="pt"
                      @click="changeImage(tumbs[0])"
                      :class="tumbs[0] === gambar_default ? 'active' : ''"
                    >
                      <img
                        src="../../public/img/products/product-2.jpg"
                        alt=""
                      />
                    </div>
                    <div
                      class="pt"
                      @click="changeImage(tumbs[1])"
                      :class="tumbs[1] === gambar_default ? 'active' : ''"
                    >
                      <img
                        src="../../public/img/products/product-4.jpg"
                        alt=""
                      />
                    </div>
                    <div
                      class="pt"
                      @click="changeImage(tumbs[2])"
                      :class="tumbs[2] === gambar_default ? 'active' : ''"
                    >
                      <img
                        src="../../public/img/products/product-8.jpg"
                        alt=""
                      />
                    </div>
                  </carousel>
                </div>
              </div>
              <div class="col-lg-6 text-left">
                <div class="product-details">
                  <div class="content">
                    <div class="pd-title">
                      <span>Start Booking</span>
                      <h3>Topi Anti Panas</h3>
                    </div>
                    <div class="pd-desc">
                      <p>
                        Minimal techno is a minimalist subgenre of techno music.
                        It is characterized by a stripped-down aesthetic that
                        exploits the use of repetition and understated
                        development. Minimal techno is thought to have been
                        originally developed in the early 1990s by Detroit-based
                        producers Robert Hood and Daniel Bell.
                      </p>
                      <h4>Rp.120.000</h4>
                    </div>
                    <div class="quantity">
                      <router-link class="primary-btn pd-cart" to="/cart-details"
                        >ADD TO CART</router-link
                      >
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- End -->
    <Youmaylove />
    <Bigsale />
    <Footer />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Youmaylove from "@/components/YouMayLoveItTo.vue";
import Footer from "@/components/Footer.vue";
import carousel from "vue-owl-carousel";

export default {
  name: "Home",
  components: {
    Navbar,
    Footer,
    carousel,
    Youmaylove,
  },
  data() {
    return {
      gambar_default: "img/products/product-2.jpg",
      tumbs: [
        "img/products/product-2.jpg",
        "img/products/product-4.jpg",
        "img/products/product-8.jpg",
      ],
    };
  },
  methods: {
    changeImage(urlImage) {
      this.gambar_default = urlImage;
    },
  },
};

window.scrollTo(0, 0);
</script>
