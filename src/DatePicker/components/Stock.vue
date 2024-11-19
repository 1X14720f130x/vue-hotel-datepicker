<template>
  <div
    v-if="show && stock"
    :class="{'stock--mobile': mobile, 'stock': !mobile }"
  >
    <span class="stock-number">{{ stock }}</span>
  </div>
</template>

<script>
export default {
  name: 'Stock',
  props: {
    show: {
      type: Boolean,
      required: true,
    },
    mobile: {
      type: Boolean,
      required: true,
    },
    stock: {
      type: String,
      required: true,
    },
  },
}
</script>

<style></style>