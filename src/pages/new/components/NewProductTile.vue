<template>
  <div class="spooky new-product-tile">
    <img :src="image" alt="" />
    <h6>{{ name }}</h6>
    <span>{{ category }}</span>
    <strong>{{ price }}</strong>
  </div>
</template>

<script lang="ts">
// import ScrollReveal from "scrollreveal";
import { Vue, Prop, Component } from "vue-property-decorator";

import SpkButton from "@/components/SpkButton.vue";

@Component({
  components: {
    SpkButton,
  },
})
export default class NewProductTile extends Vue {
  @Prop({ required: true })
  private image!: string;

  @Prop({ required: true })
  private name!: string;

  @Prop({ required: true })
  private category!: string;

  @Prop({ required: true })
  private price!: string;

  @Prop({ required: true })
  private descountPrice!: string;
}
</script>

<style scoped>
.spooky.new-product-tile {
  width: 300px;
  height: 300px;
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
  margin-right: var(--spacing-small);
  transition: all 300ms ease-in-out;
}

.spooky.new-product-tile img {
  height: 130px;
  transition: all 300ms ease-in-out;
}

.spooky.new-product-tile:hover img {
  transform: scale(1.2);
  transform-origin: center;
}
</style>
