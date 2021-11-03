<template>
  <div class="spooky new-tile">
    <img src="@/assets/images/discount-img.png" alt="" />
    <div class="text-wrapper">
      <h5>
        50% Discount <br />
        On New Product
      </h5>
      <spk-button>Go to new</spk-button>
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
}
</script>

<style scoped>
.spooky.new-tile {
  width: 200px;
  height: 200px;
  display: flex;
  cursor: pointer;
  user-select: none;
  background: linear-gradient(
    136deg,
    hsl(104, 28%, 35%) 0%,
    hsl(58, 28%, 35%) 100%
  );
  border-radius: 1rem;
  align-items: center;
  padding: var(--spacing-big);
  justify-content: space-evenly;
  transition: all 300ms ease-in-out;
}

.spooky.new-tile img {
  height: 140px;
  transition: all 300ms ease-in-out;
}

.spooky.new-tile .text-wrapper {
  width: 300px;
  text-align: center;
}

.spooky.new-tile .text-wrapper h5 {
  margin-bottom: var(--spacing-small);
}
</style>
