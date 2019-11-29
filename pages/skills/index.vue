<template lang="pug">
#skills
  h1.text-center.my-5.header-shadow Formations
  div(v-for='code in codes', :key='code.title')
    h2.mt-5.mb-4.text-center.header-shadow {{code.title}}
    .card-deck
      // <div class="card-deck my-4">
      .card.rounded-lg.border-info.text-center(v-for='card in code.content', :key='card.name')
        .card-header.bg-light
          img.card-top-img.w-100(:src='card.img', alt='')
          h5.text-right.text-muted.mt-2.float-right
            small.badge.badge-pill.badge-info.border.border-primary.float-right v{{card.version}}
        .card-body.border-top.border-info
          p.card-text
            | {{card.desc}}
            span(v-html='card.otherLogo')
        h4.card-footer.bg-info.mb-0 {{card.name}}
</template>

<script>
export default {
  name: "",
  data: () => {
    return {

      codes: [

        {
          title: "Structure",
          content: [
            {
              name: "HTML",
              version: 5.2,
              img:
                "https://juststickers.in/wp-content/uploads/2014/05/HTML5-Mark-Shape-Cut.png",
              desc: "Langage de balisage dédié au contenu du site"
            },
            {
              name: "pug",
              version: '2.0',
              img:
                "https://cdn.rawgit.com/pugjs/pug-logo/eec436cee8fd9d1726d7839cbe99d1f694692c0c/SVG/pug-final-logo-_-colour-128.svg",
              desc: 'Préprocesseur HTML - anciennement Jade ',
              otherLogo: '<img src="https://s3.amazonaws.com/oodles-technologies1/blog-images/d73085c7-ff2c-4edb-9a72-8e1333dac14e.png" width="24px" alt="">',
            },
            // {

              //   name: "Node-JS",
            //   img:
            //     "https://d2eip9sf3oo6c2.cloudfront.net/tags/images/000/000/256/full/nodejslogo.png",
            //   version: '12.13 (LTS)**',
            //   desc: "Librairie JavaScript appliquée aux serveurs"
            // }
          ]
        },
        {
          title: "Style",
          content: [
            {
              name: "CSS",
              version: 3,
              img:
                "https://cdn1.iconfinder.com/data/icons/logotypes/32/badge-css-3-512.png",
              desc: "Feuilles de style pour la mise en forme des pages"
            },
            {
              name: "Bootstrap",
              version: 4.3,
              img:
                "http://www.dxpdance.com.au/wp-content/uploads/2016/03/bootstrap-logo.jpg",
              desc: "Framework CSS facilitant la mise en forme, bibliothèque Sass"
            },
            {
              name: "Bulma",
              version: '0.8',
              img: "https://jgthms.com/web-design-in-4-minutes/bulma.png",
              desc: "Framework semblable à BootStrap, bibliothèque Sass"
            },
            {
              name: "Sass",
              version: '1.22',
              img:
                "http://www.freelogovectors.net/wp-content/uploads/2019/02/sass-logo.png",
              desc: "Préprocesseur CSS"
            }
          ]
        },
        {
          title: "Rendu",
          content: [
            {
              name: "JavaScript",
              img:
                "http://seeklogo.com/images/J/javascript-js-logo-2949701702-seeklogo.com.png?t=636356437130000000",

              version: "1.8*",
              desc: "Langage de programmation, dynamise l'application"
            },
            {
              name: "React",
              version: '16.11',
              img:
                "https://cdn4.iconfinder.com/data/icons/logos-3/600/React.js_logo-512.png",
              desc: "Framework JS facilitant la création des sites web"
            },
            {
              name: "Vue JS",
              version: '2.6',
              img:
                "http://assets.stickpng.com/thumbs/58482acecef1014c0b5e4a1e.png",
              desc: "Semblable à React, en plus simple et complet"
            },
            {
              name: "Nuxt",
              version: "2.10",
              img:
                "https://cosmic-s3.imgix.net/9af92d20-31d0-11e8-b24f-2f60c3c01c65-nuxtjs-cosmicjs.png",
              desc: "Framework utilisant VueJS pour des applis universelles "
            }
          ]
        },
        {
          title: "Autres",
          content: [
            {
              name: "Git",
              img:
                "https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Git_icon.svg/768px-Git_icon.svg.png",
              version: 2.23,
              desc: "Application servant à versionner ses codes"
            },
            {
              name: "GitHub",
              img: "http://pngimg.com/uploads/github/github_PNG40.png",
              version: 2.23,
              desc: "Le cloud des codeurs, basé sur git"
            },
            {
              name: "Python",
              version: 3.7,
              img:
                "https://cdn4.iconfinder.com/data/icons/logos-and-brands/512/267_Python_logo-512.png",
              desc:
                "Langage de programmation, plébiscité en Big Data et Machine Learning"
            }
          ]
        }
      ]
    };
  }
  /*

    */
};
</script>

<style scoped>

</style>
