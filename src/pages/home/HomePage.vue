<template>
  <section class="page" id="home">
    <flickity class="carousel" :options="flickityOptions">
      <home-slide
        v-for="(slide, index) in slides"
        :key="index"
        :image="slide.image"
        :imageHead="slide.imageHead"
        :imageSubhead="slide.imageSubhead"
        :head="slide.head"
        :subhead="slide.subhead"
        :body="slide.body"
      />
    </flickity>
  </section>
</template>

<script lang="ts">
import ScrollReveal from "scrollreveal";
import { Vue, Component } from "vue-property-decorator";

import Flickity from "vue-flickity";
import HomeSlide from "@/pages/home/components/HomeSlide.vue";

@Component({
  components: {
    Flickity,
    HomeSlide,
  },
})
export default class HomePage extends Vue {
  private flickityOptions: Record<string, any> = {
    pageDots: false,
    wrapAround: true,
    prevNextButtons: true,
  };

  private slides: Record<string, any>[] = [
    {
      image: require("@/assets/images/home1-img.png"),
      imageHead: 'The Labu "Reiza"',
      imageSubhead: "The living Pumpkin",
      head: "#1 Top Scariest Ghost",
      subhead: "Uoooo Trick or treat!!",
      body: 'Hi, I\'m Reiza, people call me "El Labu". I am currently trying to learn something new, building my own bike with parts made only in Malaysia.',
    },
    {
      image: require("@/assets/images/home2-img.png"),
      imageHead: "Adino & Grahami",
      imageSubhead: "No words can describe them",
      head: "#2 top Best duo",
      subhead: "Bring back my contton candy",
      body: "Adino steals cotton candy from his brother and eats them all in one bite, a hungry beast. Grahami can no longer contain his anger towards Adino.",
    },
    {
      image: require("@/assets/images/home3-img.png"),
      imageHead: "Captain Sem",
      imageSubhead: "Veteran Spooky Ghost",
      head: "#3 Top Scariest  Ghost",
      subhead: "Respan the spooky skull",
      body: "In search for cute little puppy, Captain Sem has come back from his tragic death. With his hogwarts certified power he promise to be a hero for all of ghostkind.",
    },
  ];

  private mounted(): void {
    // ScrollReveal().reveal(".home-carousel", {
    //   delay: 100,
    //   origin: "top",
    //   duration: 2500,
    //   distance: "60px",
    // });
  }
}
</script>

<style scoped>
.page {
  padding: 0;
}
</style>
