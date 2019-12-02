<template lang="pug">
  div
    .has-background-primary
      .container
        .media
          .media-left
            img.image.is-rounded.is-128x128(src='@/assets/img/me.jpg')
            .media-body.vertical-middle
          .media-content
            h1.title fabezio.com
            h2.subtitle Site CV de Développeur Web FrontEnd

    .container
      h2.subtitle.text-center.mb-4 Bienvenue sur ce site!
      .text-justify
        p Si vous êtes ici, c'est que vous avez besoin d'un développeur web, en freelance ou contrat interne. J'ai envie de vous dire que vous êtes au bon endroit; ceci étant, vous émettez certainement des réserves et avez besoin de preuves de mes compétences. C'est pourquoi tout est décrit ici.
        p Je vous invite donc à prendre le temps de visiter ce site et consulter
          a(href='https://github.com/Fabezio/fabezio_nuxt', target='_blank')  ma page github,
          |  afin de vous forger votre propre avis. N'hésitez pas à tester plus avant mes acquis, me faire un retour
          a(href='mailto:fabezio@outlook.fr') par mail
          |  et/ou émettre des suggestions (c'est grâce aux erreurs qu'on apprend et progresse).
        p Sur ce, je vous souhaite une bonne visite!

</template>

<script>
// import Logo from '~/components/Logo.vue'

export default {
  layout: "home",
  components: {
    // Logo
  }
};
</script>

<style lang="scss">
$info: aquamarine;
$warning: gold;
$danger: darkred;
$primary : #50c878;

body {
  font-family: 'Laconic';
  margin-top : 0;
}

.rounded-lg {
    border-radius: 1rem !important;
}

.circle {
  color: #008080;
}

.nuxt-link-exact-active {
  .circle {
    color: white !important;
  }

  &:not(.home) {
    color: darkslategrey !important;
  }
}

.media-img {
  height: 128px;
}
.loremipsum {
  padding: 1rem 0;
  margin: 1rem 0;
}
p {
  text-align: justify;
  text-indent: 1rem;

  &:first-letter {
  font-size: 1.25rem;
  }

  a {
    color: #00a86b;
    &:hover {
      text-decoration: underline #008080;
    }
  }
}

.logo {
  height: 32px;
  width: 32px;
}

nav {
  height: 2rem;
  padding: 0.5rem;
  margin-top: 0;
}
.navbar-brand {
  text-shadow: 2px 2px 2px grey;
}
.route {
  color: darkslategray;
  text-shadow: 1px 1px 1px grey;
  &:hover{
    background: $primary !important;

    .icons {
      color: whitesmoke !important;
    }

  }
}

.card {
  border: 1px solid aquamarine;
  .media-img {
  width: 128px;
  height: 128px;
  }
  /*
    */
  &:hover {
    transform: scale(1.01);
    transition: all 0.25s ease-in-out !important;
    cursor: pointer;
  }
}


.card-img-top {
background: whitesmoke;
padding: 7px;
}

@import "@/node_modules/bulma/bulma.sass";

</style>
