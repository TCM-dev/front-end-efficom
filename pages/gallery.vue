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
  </div>
</template>

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
</style>
