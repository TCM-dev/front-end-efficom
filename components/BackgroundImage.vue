<template>
  <div class="bg-image-wrapper">
    <div
      class="bg-image"
      :style="'background-image: url(' + url + '); height: ' + height + 'px;'"
    />
  </div>
</template>

<style lang="scss" scoped>
.bg-image-wrapper {
  overflow: hidden;
}

.bg-image {
  background-size: cover;
  background-position: center;
  width: 100%;
  transition: 1s;
  &:hover {
    transform: scale(1.1);
  }
}
</style>

<script>
export default {
  props: ["url", "height"]
};
</script>
