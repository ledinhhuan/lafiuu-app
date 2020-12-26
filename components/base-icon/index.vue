<template>
  <i :class="iconName" :style="{ fontSize: `${size}px` }"></i>
</template>
<script>
export default {
  props: {
    icon: {
      type: String,
      default: () => '',
    },
    size: {
      type: Number,
      default: 24,
    },
  },
  computed: {
    iconName() {
      return `icon-${this.icon}`
    },
  },
}
</script>
