<template>
  <div
    :style="'background-image: url(' + url + '); height: ' + height + 'px;'"
  />
</template>

<style lang="scss" scoped>
div {
  background-size: cover;
  background-position: center;
  width: 100%;
}
</style>

<script>
export default {
  props: ["url", "height"]
};
</script>
