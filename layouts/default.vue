<template>
  <div>
    <div class="menu" :class="hidden && 'hidden'">
      <nav>
        <h2>Navigation</h2>
        <div @click="hidden = true">
          <nuxt-link to="/">Accueil</nuxt-link>
        </div>
        <div @click="hidden = true">
          <nuxt-link to="/contact">Nous contacter</nuxt-link>
        </div>
        <div @click="hidden = true">
          <nuxt-link to="/gallery">Gallerie de photo</nuxt-link>
        </div>
        <div @click="hidden = true">
          <nuxt-link to="/about">A propos</nuxt-link>
        </div>
        <span>Nos conseils minceurs</span>
      </nav>
    </div>
    <aside>
      <span class="logo"><span class="red">FAT</span> FOOD</span>
      <button @click="hidden = !hidden">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          height="24"
          viewBox="0 0 24 24"
          width="24"
          fill="currentColor"
        >
          <path d="M0 0h24v24H0z" fill="none" />
          <path d="M3 18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z" />
        </svg>
        <span>Menu</span>
      </button>
      <nav>
        <nuxt-link to="/">Accueil</nuxt-link>
        <nuxt-link to="/contact">Nous contacter</nuxt-link>
        <nuxt-link to="/gallery">Gallerie de photo</nuxt-link>
        <nuxt-link to="/about">A propos</nuxt-link>
      </nav>
    </aside>
    <div class="container" :class="hidden && 'hidden'">
      <nuxt />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hidden: true
    };
  }
};
</script>

<style lang="scss">
.page-enter-active,
.page-leave-active {
  transition: 0.5s;
}
.page-enter,
.page-leave-active {
  opacity: 0;
}

.page-leave-active {
  transform: translateY(-50px);
}

.mobile {
  @media screen and (min-width: 800px) {
    display: none;
    visibility: hidden;
  }
}

.desktop {
  display: none;
  visibility: hidden;
  @media screen and (min-width: 800px) {
    display: inherit;
    visibility: visible;
  }
}

html {
  font-family: Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
}

*,
*:before,
*:after {
  font-family: Roboto, "Helvetica Neue", Arial, sans-serif;
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

button {
  background: none;
  border: 0;
  font-size: 100%;
}

.container {
  transform: translateY(-25px);
  transition: 600ms ease-out;

  &.hidden {
    transform: translateY(0px);
    transition: 300ms ease-in;
  }
}

body {
  background-color: hsl(220, 20, 5);
  padding-bottom: calc(65px + 2em);
  overflow-y: scroll;
  @media screen and (min-width: 800px) {
    padding-top: 60px;
  }
}

aside {
  width: 100%;
  // height: 60px;
  background: hsl(220, 20, 10);
  position: fixed;
  bottom: 0;
  border-top: solid 1px hsl(220, 20, 20);
  display: flex;
  align-items: center;
  color: hsl(220, 20, 75);
  justify-content: space-between;
  padding: 0 2em;
  z-index: 10;
  box-shadow: 0 -6px 12px rgba($color: #000, $alpha: 0.5);

  nav {
    display: none;
    visibility: hidden;
  }

  @media screen and (min-width: 800px) {
    top: 0;
    bottom: inherit;

    button {
      display: none !important;
    }

    nav {
      display: flex;
      visibility: visible;

      a {
        color: hsl(220, 20, 75);
        padding: 1.25em 2em;
        text-decoration: none;

        &.nuxt-link-exact-active {
          border-bottom: solid 2px hsl(220, 20, 75);
        }
      }
    }
  }
}

hr {
  opacity: 0;
  margin-top: 2em;

  &.half {
    margin-top: 0.5em;
  }
}

p {
  line-height: 1.5;
  list-style-position: inside;
}

.content {
  padding: 0 2rem;
  width: 100%;
  color: hsl(220, 20, 75);

  @media screen and (min-width: 800px) {
    max-width: 1000px;
    margin: auto;
  }

  img {
    width: 100%;
  }

  strong {
    color: hsl(220, 20, 85);
  }
}
</style>

<style lang="scss" scoped>
button {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  // flex: 1;
  padding: 0.625em 1em;
  color: hsl(220, 20, 75);

  span {
    margin-top: 0.5em;
    font-size: 12px;
    font-weight: bold;
    text-transform: uppercase;
  }
}

.flex-row {
  display: flex;
}

.logo {
  font-weight: bold;
  font-size: 1.5em;
  color: orange;
  padding: 0 1em;

  .red {
    color: orangered;
  }
}

.menu {
  position: fixed;
  width: 100%;
  height: 100vh;
  z-index: 2;
  top: 0;
  background: hsl(220, 20, 5);
  transform: translateY(0px);
  opacity: 1;
  visibility: visible;
  transition: visibility 0s linear 0s, opacity 300ms ease-out,
    transform 300ms ease-out;

  &.hidden {
    transform: translateY(25px);
    visibility: hidden;
    opacity: 0;
    transition: visibility 0s linear 300ms, opacity 300ms ease-in,
      transform 300ms ease-in;
  }

  nav {
    display: flex;
    flex-direction: column;
    padding: 2em;

    a {
      padding: 0.625em 0;
      font-weight: 600;
      text-decoration: none;
      color: hsl(220, 20, 75);
      font-size: 1.5em;
      display: block;
    }

    span {
      padding: 0.625em 0;
      font-weight: 600;
      color: hsl(220, 20, 40);
      font-size: 1.5em;
      display: block;
    }

    h2 {
      font-weight: 600;
      color: hsl(220, 20, 90);
      font-size: 2em;
      margin-bottom: 1em;
    }
  }
}
</style>
