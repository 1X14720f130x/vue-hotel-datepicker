<template>
  <div
    v-if="show && price"
    :class="{
      'price--mobile': mobile, 'price': !mobile }"
  >
    <span class="price-number">{{ price }}</span>
    <span class="price-symbol">{{ symbol }}</span>
  </div>
</template>

<script>
export default {
  name: 'Price',
  props: {
    show: {
      type: Boolean,
      required: true,
    },
    mobile: {
      type: Boolean,
      required: true,
    },
    price: {
      type: String,
      required: true,
    },
    symbol: {
      type: [String, null, undefined],
      default: '',
    },
  },
}
</script>

<style></style>
