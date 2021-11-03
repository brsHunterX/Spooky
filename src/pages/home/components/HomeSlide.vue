<template>
  <div class="spooky home-slide">
    <div class="image-wrapper">
      <img :src="image" alt="Illustration" />
      <div class="image-legend">
        <h6>{{ imageHead }}</h6>
        <span>{{ imageSubhead }}</span>
      </div>
    </div>
    <div class="text-wrapper">
      <h4>{{ head }}</h4>
      <h1>{{ subhead }}</h1>
      <p>{{ body }}</p>
      <div class="text-footer">
        <spk-button> Book Now </spk-button>
        <span>Track record <i class="bx bx-right-arrow-alt"></i></span>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, Prop, Component } from "vue-property-decorator";

import SpkButton from "@/components/SpkButton.vue";

@Component({
  components: {
    SpkButton,
  },
})
export default class HomeSlide extends Vue {
  @Prop({ required: true })
  private image!: string;

  @Prop({ required: true })
  private imageHead!: string;

  @Prop({ required: true })
  private imageSubhead!: string;

  @Prop({ required: true })
  private head!: string;

  @Prop({ required: true })
  private subhead!: string;

  @Prop({ required: true })
  private body!: string;
}
</script>

<style scoped>
.spooky.home-slide {
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.spooky.home-slide .image-wrapper {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.spooky.home-slide .image-wrapper img {
  height: 420px;
}

.spooky.home-slide .image-wrapper .image-legend {
  display: flex;
  position: relative;
  align-items: flex-end;
  flex-direction: column;
  margin-top: var(--spacing-big);
  padding: var(--spacing-big) var(--spacing-big) 0 0;
}

.spooky.home-slide .image-wrapper .image-legend::before {
  top: 0;
  right: 0;
  width: 1px;
  content: "";
  height: 100%;
  background: #fff;
  position: absolute;
}

.spooky.home-slide .image-wrapper .image-legend::after {
  top: -8px;
  width: 9px;
  height: 9px;
  right: -4px;
  content: "";
  position: absolute;
  background: #fff;
  border-radius: 999px;
}

.spooky.home-slide .text-wrapper {
  width: 450px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-end;
  margin-left: var(--spacing-biggest);
}

.spooky.home-slide .text-wrapper h1 {
  text-transform: uppercase;
  margin: var(--spacing-medium) 0;
}

.spooky.home-slide .text-wrapper .text-footer {
  width: 100%;
  display: flex;
  align-items: center;
  margin-top: var(--spacing-big);
  justify-content: space-between;
}

.spooky.home-slide .text-wrapper .text-footer span {
  display: flex;
  align-items: center;
  color: var(--color-head-text);
  font-weight: var(--text-medium);
  font-size: var(--text-normal-size);
  font-family: var(--text-primary-font-family);
}

.spooky.home-slide .text-wrapper .text-footer span i {
  font-size: 22px;
}
</style>
