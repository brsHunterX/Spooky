<template>
  <button class="spooky">
    <slot></slot>
  </button>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

@Component({})
export default class SpkButton extends Vue {}
</script>

<style scoped>
button.spooky {
  margin: 0;
  padding: 0;
  width: auto;
  border: none;
  cursor: pointer;
  appearance: none;
  overflow: visible;
  padding: 1rem 2rem;
  border-radius: 8px;
  line-height: normal;
  background: var(--color-primary);
  transition: all 300ms ease-in-out;
}

button.spooky:hover {
  filter: brightness(95%);
}
</style>
