<template>
  <section class="page" id="about">
    ABOUT
    <!-- <div class="wrapper">
      <div class="text-wrapper" id="about-text">
        <h2>About Halloween Night</h2>
        <p>
          Night of all the saints, or all the dead, is celebrated on October 31
          and it is a very fun international celebration, this celebration comes
          from ancient origins, and is already celebrated by everyone.
        </p>
        <spk-button>Know more</spk-button>
      </div>
      <img
        id="about-image"
        src="@/assets/images/about-img.png"
        alt="About Illustration"
      />
    </div> -->
  </section>
</template>

<script lang="ts">
import ScrollReveal from "scrollreveal";
import { Vue, Component } from "vue-property-decorator";

import SpkButton from "@/components/SpkButton.vue";

@Component({
  components: {
    SpkButton,
  },
})
export default class AboutPage extends Vue {
  private mounted(): void {
    // ScrollReveal().reveal("#about-text", {
    //   delay: 100,
    //   origin: "left",
    //   duration: 3000,
    //   distance: "80px",
    // });

    // ScrollReveal().reveal("#about-image", {
    //   delay: 100,
    //   origin: "right",
    //   duration: 3000,
    //   distance: "80px",
    // });
  }
}
</script>

<style scoped>
section.spooky.about {
  width: 100%;
  height: 100vh;
  display: flex;
  align-content: center;
  justify-content: center;
  padding-top: var(--layout-header-height);
}

section.spooky.about .wrapper img {
  height: 480px;
}

section.spooky.about .wrapper .text-wrapper {
  width: 450px;
}

section.spooky.about .wrapper .text-wrapper p {
  width: 450px;
  margin: var(--spacing-big) 0;
}
</style>
