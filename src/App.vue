<template>
  <main>
    <spk-nav-header :elevated="!inTop" />
    <home-page />
    <category-page />
    <about-page />
    <product-page />
    <new-page />
  </main>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

// COMPONENTS
import SpkNavHeader from "@/components/SpkNavHeader.vue";

// PAGES
import HomePage from "@/pages/home/HomePage.vue";
import CategoryPage from "@/pages/category/CategoryPage.vue";
import AboutPage from "@/pages/about/AboutPage.vue";
import ProductPage from "@/pages/product/ProductPage.vue";
import NewPage from "@/pages/new/NewPage.vue";

@Component({
  components: {
    SpkNavHeader,
    HomePage,
    CategoryPage,
    AboutPage,
    ProductPage,
    NewPage,
  },
})
export default class App extends Vue {
  private inTop: boolean = true;

  private handleScroll(): void {
    this.inTop = window.scrollY <= 0;
  }

  public created(): void {
    window.addEventListener("scroll", this.handleScroll);
  }

  public destroyed(): void {
    window.removeEventListener("scroll", this.handleScroll);
  }
}
</script>

<style>
@import url("./assets/css/main.css");
</style>
