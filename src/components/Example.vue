<template>
  <div>
    <item-grid
      min-width="100px"
    >
      <div
        v-for="i in 12"
        :key="`item-${i}`"
        :class="$style.testItem"
      >
        <span :class="$style.itemTitle">Item {{ i }}</span>
      </div>
    </item-grid>

    <div :class="$style.withSidebar">
      <aside :class="$style.sidebar"> fixed width sidebar</aside>
      <item-grid
        min-width="100px"
      >
        <div
          v-for="i in 12"
          :key="`item-${i}`"
          :class="$style.testItem"
        >
          <span :class="$style.itemTitle">Item {{ i }}</span>
        </div>
      </item-grid>
    </div>
  </div>
</template>

<script>
import ItemGrid from './ItemGrid.vue';

export default {
  name: 'Example',
  components: { ItemGrid },
};
</script>

<style module lang="scss">
.testItem {
  background-color: silver;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 5em;
}

.itemTitle {
  color: black;
}

.withSidebar {
  display: grid;
  grid-template-columns: 200px auto;
  gap: 1em;
  margin-top: 2em;
}
.sidebar {
  border-right: 2px solid silver;
}

</style>
