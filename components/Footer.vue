<template lang="pug">
  footer.has-background-primary.footer.has-text-centered
    nav.navbar.has-background-primary.is-fixed-bottom.is-centered
      // elements principaux
      div.navbar-item(v-for='link in links', :key='link.route')
        nuxt-link.navbar-item.route(:to='link.route')
          div.icon
            IconStack(:faClass='link.icon')
          .subtitle.is-4 {{link.name }}
      div.navbar-item.route(href='https://github.com/Fabezio/fabezio_nuxt', target='_blank')
        div.icon
          IconStack(faClass='fab fa-github-alt')
        .subtitle.is-4 mon code source
    p.is-centered Tous droits réservés - fabezio.fr
      span &copy; 2019

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
