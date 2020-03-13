<template>
  <div>
    <background-image url="/banner.jpg" height="200" class="mobile" />
    <background-image url="/banner.jpg" height="500" class="desktop" />
    <hr />
    <div class="content">
      <h1>Bienvenue chez FAT FOOD !</h1>
      <br />
      <p>
        Chez <strong>FAT FOOD</strong> nos hamburgers sont tout simplement
        énormes, notre bannière montre un hamburger de 45cm de hauteur et c'est
        le plus petit sur notre menu !
      </p>
      <hr />
      <background-image url="/vache.jpg" height="300" />
      <hr class="half" />
      <p>
        Cette vache s'appelle <strong>Mélanie</strong> et est à l'origine du
        steak présent dans l'hamburger de la photo. Nos vaches sont spécialement
        sélectionnées parmis les moins sportives et leurs parties parmies les plus grasses.
        Pour un maximum de goût, et de gras...
      </p>
      <hr />
      <div class="flex-row">
        <background-image url="/burger.jpg" height="400" />
        <div>
          <hr class="half mobile" />
          <p>
            Voici le plus gros hamburger sur notre menu ! Il fait
            <strong>75cm</strong> de hauteur. Mais ne vous détrompez pas, la
            taille compte car ces quelques 30cm de différence font que ce ne
            sont pas moins de 3 vaches qui s'y sont misent jusqu'au cou !
          </p>
          <hr class="half" />
          <p>
            Notre menu
          </p>
          <ul>
            <li>
              Le <strong>45</strong> : en ce moment à 150€ au lieu de 180€ pour
              les étudiants !
            </li>
            <li>
              Le <strong>60</strong> : 300€ mais les frites sont offertes !
            </li>
            <li>
              Le <strong>75</strong> : 450€, près de 40Kg de viandes mais
              surtout 2 heures de cuissons et 4 boulangers pour préparer le pain
              !
            </li>
          </ul>
        </div>
      </div>
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
.banner {
  width: 100%;
  height: 200px;
  background-image: url("/banner.jpg");
  background-size: cover;
  background-position: center;

  @media screen and (min-width: 800px) {
    height: 500px;
  }
}

.flex-row {
  @media screen and (min-width: 800px) {
    display: flex;
    flex-direction: row-reverse;

    & > * {
      flex: 1;
    }

    & > div:first-child {
      margin-left: 1em;
    }
  }
}
</style>
