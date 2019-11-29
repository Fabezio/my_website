<template lang="pug">
  div
    div.media.border-top.border-secondary.p-3.bg-primary
    div.container
      img.align-self-start.media-img.border.border-dark.mr-3.rounded-lg.float-left(src='@/assets/img/me.jpg')
      .media-body.vertical-middle
        h1.title fabezio.com
        h2.subtitle Site CV de Développeur Web FrontEnd

    div.container.my-5
      h2.subtitle.text-center.mb-4 Bienvenue sur ce site!
      .text-justify
        p Si vous êtes ici, c'est que vous avez besoin d'un développeur web. J'ai envie de vous dire que vous êtes au bon endroit; ceci étant, vous émettez certainement des réserves et avez besoin de preuves de mes compétences. C'est pourquoi tout est décrit ici.
        p Je vous invite donc à prendre le temps de visiter ce site, consulter
          a(href='https://github.com/Fabezio/fabezio_nuxt', target='_blank') ma page github, afin de vous forger votre propre avis. N'hésitez pas à tester plus avant mes acquis, me faire un retour
          a(href='mailto:fabezio@outlook.fr') par mail et/ou émettre des suggestions (c'est grâce aux erreurs qu'on apprend et progresse).
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
$secondary: #00a86b;
$warning: gold;
$danger: darkred;
$primary : #50c878;

body {
  font-family: 'Laconic';
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
  /*
  .nav-icon {
    background: #00a86b !important;
    background-color: none;
    color: aquamarine !important;
  }
  */
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
.card {
  .media-img {
  width: 128px;
  height: 128px;
  }
    border: 1px solid aquamarine;
    /*
     */
    &:hover {
      transform: scale(1.15);
      transition: all 0.25s ease-in-out !important;
      cursor: pointer;
    }
  }
  /*
.card-footer {
  background: aquamarine;
  color: #5c5c5c;
text-shadow: 0.5px 0.5px darkslateblue;
}
*/

.card-img-top {
background: whitesmoke;
padding: 7px;
}

/*
#my-card {
  vertical-align: middle;
  border: none;
  transition: none;
}
.btn-gold {
  background: gold;
}
.bg-green {
  background: green;
}

.bg-emerald {
  background: #50c878;
}
.bg-turquoise {
  background: aquamarine;
}
.bg-jade {
  background: #00a86b;
}
.far,
.fas {
  margin: 0 !important;
}
.bg-transparent {
  background: rgba (0, 0, 0, 0.25) !important;
}
.bg-teal {
  background: #008080;
}
.bg-bluesky {
    background: skyblue;
}
.card-img-top img {
  max-height: 213px !important;
  min-height: 213px !important;
  height: auto !important;
  max-width: 213px !important;
  width: auto !important;
} */


/* .card-body {
    border-top: 1px solid aquamarine;
    border-bottom: 1px solid aquamarine;
    .teal-circle {
      color: #008080;
    }
  } */




/*

.fab.route:active,
.fas.route:active,
.nuxt-link-exact-active .this-fa,
.navbar-brand {
  color: white !important;

}
.nav-link {
  color: silver !important;
}
*/
/* .nav-tabs :active {
    background: whitesmoke;
  } */


// @import "../../node_modules/bootstrap/scss/variables";


@import "@/node_modules/bulma/bulma.sass";


</style>
