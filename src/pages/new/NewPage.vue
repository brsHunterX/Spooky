<template>
  <section class="page" id="news">
    NEWS
    <!-- <div class="wrapper">
      <h2>New Arrivals</h2>
      <flickity class="carousel" ref="flickity" :options="flickityOptions">
        <new-product-tile
          v-for="(item, index) in news"
          :key="index"
          :image="item.image"
          :name="item.name"
          :category="item.category"
          :price="item.price"
          :descountPrice="item.descountPrice"
        />
      </flickity>
      <h2>Our Newslatter</h2>
      <p>Promotion new products and sales. Directly to your inbox</p>
      <news-letter-input />
    </div> -->
  </section>
</template>

<script lang="ts">
import ScrollReveal from "scrollreveal";
import { Vue, Component } from "vue-property-decorator";

import Flickity from "vue-flickity";
import NewProductTile from "@/pages/new/components/NewProductTile.vue";
import NewsLetterInput from "@/pages/new/components/NewsLetterInput.vue";

@Component({
  components: {
    Flickity,
    NewProductTile,
    NewsLetterInput,
  },
})
export default class NewPage extends Vue {
  private flickityOptions: Record<string, any> = {
    pageDots: false,
    wrapAround: true,
    prevNextButtons: false,
  };

  private news: Record<string, any>[] = [
    {
      image: require("@/assets/images/new1-img.png"),
      name: "Haunted House",
      category: "Accessory",
      price: "$14.99",
      descountPrice: "$29.99",
    },
    {
      image: require("@/assets/images/new2-img.png"),
      name: "Halloween Candle",
      category: "Accessory",
      price: "$11.99",
      descountPrice: "$21.99",
    },
    {
      image: require("@/assets/images/new3-img.png"),
      name: "Witch Broom",
      category: "Accessory",
      price: "$7.99",
      descountPrice: "$14.99",
    },
    {
      image: require("@/assets/images/new4-img.png"),
      name: "Rip",
      category: "Accessory",
      price: "$24.99",
      descountPrice: "$44.99",
    },
    {
      image: require("@/assets/images/new5-img.png"),
      name: "Terrifying Crystal Ball",
      category: "Accessory",
      price: "$5.99",
      descountPrice: "$12.99",
    },
    {
      image: require("@/assets/images/new6-img.png"),
      name: "Witch Hat",
      category: "Accessory",
      price: "$4.99",
      descountPrice: "$9.99",
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
section.spooky.news {
  width: 100%;
  height: 100vh;
  display: flex;
  align-content: center;
  justify-content: center;
  padding-top: var(--layout-header-height);
}

/* section.spooky.news .wrapper {
  width: 1000px;
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
} */

section.spooky.news .wrapper p {
  width: 300px;
  text-align: center;
  margin: var(--spacing-big) 0;
}

section.spooky.news .wrapper .carousel {
  width: 100%;
  margin: var(--spacing-biggest) 0;
}
</style>
