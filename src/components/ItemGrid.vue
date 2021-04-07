<template>
  <div :class="$style.itemGrid" :style="gridStyle">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'item-grid',
  props: {
    minWidth: {
      type: String,
      default: '200px',
    },
    maxWidth: {
      type: String,
      default: '1fr',
    },
    gapHorizontal: {
      type: String,
      default: '1em',
    },
    gapVertical: {
      type: String,
      default: '1em',
    },
  },
  computed: {
    gridStyle() {
      return {
        color: 'red',
        'grid-template-columns': `repeat(auto-fill, minmax(${this.minWidth}, ${this.maxWidth})`,
        gap: `${this.gapHorizontal} ${this.gapVertical}`,
      };
    },
  },
};
</script>

<style module lang="scss">
.itemGrid {
  display: grid;
}
</style>
