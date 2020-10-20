<template>
  <section class="partner-component">
    <div class="container">
      <div class="row">
        <div
          class="col"
          v-for="partners in DataDumy.partner"
          v-bind:key="partners._id"
        >
          <img :src="partners.imageUrl" class="card-img-top" />
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
  name: "Partner",
};
</script>
