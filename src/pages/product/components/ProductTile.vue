<template>
  <div class="spooky product-tile">
    <img :src="image" alt="" />
    <h6>{{ name }}</h6>
    <span>{{ category }}</span>
    <strong>{{ price }}</strong>
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
export default class ProductTile extends Vue {
  @Prop({ required: true })
  private image!: string;

  @Prop({ required: true })
  private name!: string;

  @Prop({ required: true })
  private category!: string;

  @Prop({ required: true })
  private price!: string;
}
</script>

<style scoped>
.spooky.product-tile {
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
  flex-direction: column;
  justify-content: center;
  padding: var(--spacing-big);
  transition: all 300ms ease-in-out;
}

.spooky.product-tile:hover {
  transform: scale(1.1);
}

.spooky.product-tile img {
  height: 80px;
  transition: all 300ms ease-in-out;
}

.spooky.product-tile:hover img {
  transform-origin: center;
  transform: scale(1.2) rotate(-15deg);
}
</style>
