<template>
  <section class="page" id="category">
    CATEGORY
    <!-- <div class="wrapper">
      <h2>Favorite Scare Category</h2>
      <div class="grid">
        <category-tile v-for="(category, index) in categories" :key="index" />
        <div style="background: red">Item</div>
        <div style="background: red">Item</div>
        <div style="background: red">Item</div>
        <div style="background: red">Item</div>
        <div style="background: red">Item</div>
      </div>
    </div> -->
  </section>
</template>

<script lang="ts">
import ScrollReveal from "scrollreveal";
import { Vue, Component } from "vue-property-decorator";

import CategoryTile from "@/pages/category/components/CategoryTile.vue";

@Component({
  components: {
    CategoryTile,
  },
})
export default class CategoryPage extends Vue {
  private categories: Record<string, any>[] = [
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
section.spooky.categories {
  width: 100%;
  display: flex;
  align-content: center;
  justify-content: center;
  padding-top: var(--layout-header-height);
}
</style>
