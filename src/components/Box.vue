<script>
export default {
  name: 'Box',
}
</script>

<template>
  <div class="box">
    <slot />
  </div>
</template>

<style lang="scss" scoped>
.box {
  padding: 16px;
}
</style>
