<template functional>
  <div>
    <div v-if="props.isLoading">
      <slot name="loader"/>
    </div>
    <slot v-else name="content"/>
  </div>
</template>

<script>
export default {
  name: "loading-container",
  props: {
    isLoading: {
      type: Boolean,
      default: false
    }
  }
};
</script>