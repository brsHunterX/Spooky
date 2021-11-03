<template>
  <section class="page" id="products">
    PRODUCTS
    <!-- <div class="wrapper">
      <h2>Trick Or Treat</h2>
      <div class="grid">
        <product-tile
          v-for="(product, index) in products"
          :key="index"
          :image="product.image"
          :name="product.name"
          :category="product.category"
          :price="product.price"
        />
      </div>
    </div> -->
  </section>
</template>

<script lang="ts">
import ScrollReveal from "scrollreveal";
import { Vue, Component } from "vue-property-decorator";

import NewTile from "@/pages/product/components/NewTile.vue";
import ProductTile from "@/pages/product/components/ProductTile.vue";

@Component({
  components: {
    NewTile,
    ProductTile,
  },
})
export default class CandyPage extends Vue {
  private products: Record<string, any>[] = [
    {
      image: require("@/assets/images/trick-treat1-img.png"),
      name: "Toffee",
      category: "Candy",
      price: "$11.99",
    },
    {
      image: require("@/assets/images/trick-treat2-img.png"),
      name: "Bone",
      category: "Accessory",
      price: "$8.99",
    },
    {
      image: require("@/assets/images/trick-treat3-img.png"),
      name: "Scarecrow",
      category: "Accessory",
      price: "$15.99",
    },
    {
      image: require("@/assets/images/trick-treat4-img.png"),
      name: "Candy Cane",
      category: "Candy",
      price: "$7.99",
    },
    {
      image: require("@/assets/images/trick-treat5-img.png"),
      name: "Pumpkin",
      category: "Candy",
      price: "$19.99",
    },
    {
      image: require("@/assets/images/trick-treat6-img.png"),
      name: "Ghost",
      category: "Accessory",
      price: "$17.99",
    },
  ];

  private mounted(): void {
    // ScrollReveal().reveal(".wrapper", {
    //   delay: 100,
    //   origin: "top",
    //   duration: 3000,
    //   distance: "80px",
    // });
  }
}
</script>

<style scoped>
section.spooky.products {
  width: 100%;
  height: 100vh;
  display: flex;
  align-content: center;
  justify-content: center;
  padding-top: var(--layout-header-height);
}

/* section.spooky.products .wrapper {
  width: 1000px;
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
} */

section.spooky.products .wrapper h2 {
  margin-bottom: var(--spacing-biggest);
}

/* section.spooky.products .wrapper .grid {
  display: grid;
  grid-auto-rows: 300px;
  gap: var(--spacing-big);
  grid-template-columns: repeat(3, 300px);
} */
</style>
