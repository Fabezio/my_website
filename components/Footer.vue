<template lang="pug">
  div.has-background-primary
    footer.footer.d-block.mx-auto.py-3.bg-primary.text-dark.font-weight-light
      b-nav(type='dark', align='center', pils='')
        // elements principaux
        b-nav-item.nav-item.nav-pill(v-for='link in links', :key='link.route')
          nuxt-link.nav-link(:to='link.route')
            iconstack(:faclass='link.icon')
              span.route {{link.name | capitalize({onlyFirstLetter: true}) }}
        b-nav-item(href='https://github.com/Fabezio/fabezio_nuxt', target='_blank')
          iconstack(faclass='fab fa-github-alt')
            span.route Mon code source
      p.is-centered Tous droits réservés - fabezio.fr
        span © 2019

</template>

<script>
import IconStack from "@/components/IconStack";
export default {
  name: "Footer",
  components: {
    IconStack
  },
  data() {
    return {
      links: [
        {
          route: "/map",
          name: "plan du site",
          icon: "far fa-map"
        },
        {
          route: "/cgu",
          name: "conditions",
          icon: "fas fa-file-contract"
        },
        {
          route: "/help",
          name: "aide",
          icon: "fas fa-question"
        }
        // {
        //   route: "/faq",
        //   name: "foire aux questions",
        //   icon: "fas fa-question-circle"
        // },
      ]
    };
  }
};
</script>
