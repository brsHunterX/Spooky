<template>
  <div class="spooky category-tile">
    <img src="@/assets/images/category1-img.png" alt="" />
    <h6>Ghosts</h6>
    <p>Choose the ghosts, the scariest there are.</p>
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
export default class CategoryTile extends Vue {
  @Prop({ required: true })
  private image!: string;
}
</script>

<style scoped>
.spooky.category-tile {
  /* display: flex; */
  cursor: pointer;
  user-select: none;
  background: red;
  border-radius: 1rem;
  /* text-align: center; */
  /* align-items: center; */
  /* flex-direction: column; */
  /* justify-content: center; */
  padding: var(--spacing-big);
  transition: all 300ms ease-in-out;
}

.spooky.category-tile img {
  height: 130px;
  transition: all 300ms ease-in-out;
}

.spooky.category-tile p {
  width: 250px;
  transition: all 300ms ease-in-out;
}
</style>
