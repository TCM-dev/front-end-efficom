<template>
  <div class="content">
    <h1>Gallerie photo</h1>
    <hr class="half" />
    <p>
      Nos vaches sont des stars internationales et sont photographiées par tous
      les plus grands photographes et paparazis.
      <br />
      <br />
      Voici quelques photos d'elles et de leurs <strong>oeuvres</strong>.
    </p>
    <hr />
    <div class="flex">
      <div>
        <img src="/vache.jpg" alt="" />
        <h2>Titre de l'image</h2>
        <p>Description de l'image</p>
      </div>
      <div>
        <img src="/burger.jpg" alt="" />
        <h2>Titre de l'image</h2>
        <p>Description de l'image</p>
      </div>
      <div>
        <img src="/banner.jpg" alt="" />
        <h2>Titre de l'image</h2>
        <p>Description de l'image</p>
      </div>
      <div>
        <img src="/vache.jpg" alt="" />
        <h2>Titre de l'image</h2>
        <p>Description de l'image</p>
      </div>
    </div>
    <h2>Je savais pas trop où placer ça</h2>
    <p>Du coup je fais ça ici</p>
    <br />
    <div class="flex-row">
      <background-image url="/burger.jpg" height="200" />
      <div>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ut, fuga?
          Illo perferendis omnis ratione cumque corporis, sapiente repellendus
          quis laboriosam est voluptate mollitia incidunt velit atque natus
          laborum impedit expedita!
        </p>
      </div>
    </div>
    <div class="flex-row">
      <div class="flex-col">
        <div class="flex-row">
          <background-image url="/vache.jpg" height="250" />
          <background-image url="/burger.jpg" height="250" />
        </div>
        <p class="paragraph">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ut, fuga?
          Illo perferendis omnis ratione cumque corporis, sapiente repellendus
          quis laboriosam est voluptate mollitia incidunt velit atque natus
          laborum impedit expedita!
        </p>
      </div>
      <background-image url="/banner.jpg" height="500" />
    </div>
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

  img {
    margin-bottom: 1em;
  }

  div {
    margin-bottom: 2em;
  }

  @media screen and (min-width: 800px) {
    width: 100%;
    flex-wrap: nowrap;
    justify-content: space-between;

    div {
      flex: 1;
    }

    div:not(:first-of-type) {
      margin-left: 1em;
    }

    img {
      margin-top: 0;
      width: 100%;
    }
  }
}

.bg-image-wrapper,
.paragraph {
  margin-bottom: 1em;

  @media screen and (min-width: 800px) {
    margin-bottom: initial;
  }
}

.flex-col {
  display: flex;
  flex-direction: column;

  p {
    flex: 1;
  }
}

.flex-row {
  display: flex;
  flex-direction: column;
  margin-bottom: 1em;

  @media screen and (min-width: 800px) {
    flex-direction: row;
    div {
      flex: 1;
      flex-shrink: 0;
    }

    & > div:first-of-type {
      margin-right: 1em;
    }
  }
}
</style>
