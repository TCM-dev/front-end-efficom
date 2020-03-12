<template>
  <div class="content">
    <h1>A propos</h1>
    <hr class="half" />
    <background-image url="/vache.jpg" height="200" class="mobile" />
    <background-image url="/vache.jpg" height="400" class="desktop" />
    <hr class="half" />
    <p>
      Nos produits sont tous composés de viandes. La salade est constituée
      synthètiquement à partir de jambon avec des colorants verts. Le pain est
      préparé en mélangeant la pâte avec de la graisse et du bacon fumé. La
      farine est également constituée de poudre animale.
    </p>
  </div>
</template>

<script>
import BackgroundImage from "~/components/BackgroundImage";
export default {
  components: {
    BackgroundImage
  }
};
</script>

<style lang="scss" scoped>
.content {
  margin-top: 2em;
}

.flex {
  display: flex;
  flex-wrap: wrap;

  img:not(:first-of-type) {
    margin-top: 2em;
  }
}
</style>
