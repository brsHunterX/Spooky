<template>
  <header class="spooky" :class="[elevatedClass]">
    <nav>
      <a href="#home">
        <img src="@/assets/images/logo.png" alt="Logo" />
      </a>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#products">Products</a></li>
        <li><a href="#news">News</a></li>
      </ul>
    </nav>
  </header>
</template>

<script lang="ts">
import { Vue, Prop, Component } from "vue-property-decorator";

@Component({})
export default class SpkNavHeader extends Vue {
  @Prop({ type: Boolean, default: false })
  private elevated!: boolean;

  private get elevatedClass(): string | null {
    return this.elevated ? "elevated" : null;
  }
}
</script>

<style scoped>
header.spooky {
  width: 100%;
  z-index: 999;
  display: flex;
  position: fixed;
  align-items: center;
  justify-content: center;
  transition: all 300ms ease-in-out;
  height: var(--layout-header-height);
}

header.spooky nav {
  height: 100%;
  width: 1000px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

header.spooky nav a img {
  height: 2rem;
}

header.spooky nav ul {
  display: flex;
}

header.spooky nav ul li a {
  cursor: pointer;
  transition: all 300ms ease-in-out;
}

header.spooky nav ul li a:hover {
  color: var(--color-head-text);
}

header.spooky.elevated {
  backdrop-filter: blur(15px);
  background: var(--color-background-header);
}
</style>
