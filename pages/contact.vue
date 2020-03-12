<template>
  <div class="content">
    <h1>Contactez-nous !</h1>
    <hr class="half" />
    <p>
      Si vous êtes végan, sachez que nous n'aimons pas ceux qui mangent la nourriture de notre nourriture, alors passez votre chemin !
      <br />Sinon vous pouvez nous contacter via ce formulaire pour toutes vos questions.
    </p>
    <form method="POST" action="https://~°API-FAT-FOOD°~.com/contact">
      <label for="sujet">Objet</label>
      <input type="text" id="sujet" name="sujet" />
      <label for="email">E-mail</label>
      <input type="email" id="email" name="email" />
      <label for="content">Contenu</label>
      <textarea id="content" name="content" rows="10" />
      <button>Envoyer</button>
    </form>
  </div>
</template>

<style lang="scss" scoped>
.content {
  margin-top: 2em;
}

label {
  margin-top: 1em;
  display: block;
  font-weight: 500;
}

input, textarea {
  margin-top: 0.5em;
  padding: 1em;
  border-radius: 0.25em;
  border: solid 2px hsl(200, 40, 70);
  background: transparent;
  width: 100%;
}

button {
  background: hsl(200, 40, 70);
  padding: 0.625em 1em;
  width: 100%;
  border-radius: 0.25em;
  margin-top: 2em;
}
</style>
