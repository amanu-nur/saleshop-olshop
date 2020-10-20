<template>
  <section class="product-section">
    <div class="container">
      <h2 class="title-product text-left">Flash Sale</h2>
      <div class="row">
        <div
          class="col-lg"
          v-for="flash in DataDumy.flash_sale"
          v-bind:key="flash._id"
        >
          <router-link to="/product-details">
            <div class="card">
              <img :src="flash.imageUrl" class="card-img-top" />
              <div class="card-body">
                <div class="row">
                  <div class="col text-left">
                    <p class="text-title-product ">{{ flash.name }}</p>
                    <p class="product-price">
                      Rp.{{ flash.discount }} /
                      <span>Rp.{{ flash.price }}</span>
                    </p>
                  </div>
                  <div class="col-2">
                    <a href="#">
                      <i class="far fa-heart fa-lg"></i>
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </router-link>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import DataDumy from "@/Dumy/products.json";

export default {
  data: function() {
    return {
      DataDumy,
    };
  },
  name: "Flashsale",
};
</script>
