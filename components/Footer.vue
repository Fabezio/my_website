<template lang="pug">
  footer.has-background-primary.footer.d-block.mx-auto.py-3.bg-primary.text-dark.font-weight-light.is-centered
    nav.navbar.has-background-primary
      // elements principaux
      div.nav-item.nav-pill(v-for='link in links', :key='link.route')
        nuxt-link.nav-link.is-inline.columns(:to='link.route')
          IconStack.is-float-left.column(:faClass='link.icon')
          i.route.is-uppercase.column {{link.name }}
      div(href='https://github.com/Fabezio/fabezio_nuxt', target='_blank')
        IconStack(faClass='fab fa-github-alt')
          span.route.is-uppercase Mon code source
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
