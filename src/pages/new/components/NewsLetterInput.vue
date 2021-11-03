<template>
  <div class="spooky news-letter-input">
    <input type="text" placeholder="Enter your email" v-model="email" />
    <spk-button> Subscribe </spk-button>
  </div>
</template>

<script lang="ts">
// import ScrollReveal from "scrollreveal";
import { Vue, Component } from "vue-property-decorator";

import SpkButton from "@/components/SpkButton.vue";

@Component({
  components: {
    SpkButton,
  },
})
export default class NewsLetterInput extends Vue {
  private email: string = "";
}
</script>

<style scoped>
.spooky.news-letter-input {
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
  justify-content: space-between;
  padding: var(--spacing-medium);
  transition: all 300ms ease-in-out;
}

.spooky.news-letter-input input {
  width: 300px;
  border: none;
  outline: none;
  box-shadow: none;
  background-image: none;
  background-color: transparent;
  color: var(--color-label-text);
  margin-right: var(--spacing-big);
}

.spooky.news-letter-input input::placeholder {
  color: var(--color-label-text);
}
</style>
