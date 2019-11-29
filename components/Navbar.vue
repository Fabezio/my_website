<template lang="pug">
  nav.navbar.is-primary.is-top-fixed(role='navigation', aria-label='main navigation')
    div.navbar-brand
      img.logo(src='@/assets/favicon-32.png', alt='logo', title='logo')
      nuxt-link.subtitle.is-lowercase(to='/') fabezio.com

      a.navbar-burger.burger(role='button', aria-label='menu', aria-expanded='false', data-target='navbarBasicExample', @click="navToggle = isActive")
        span(aria-hidden='true')
        span(aria-hidden='true')
        span(aria-hidden='true')

    div#navbarBasicExample.navbar-menu
      .navbar-start
        div(v-for='link in links', :key='link.route')
          nuxt-link.nav-link(:to='link.route')
            iconstack(:faclass='link.icon')
            span.route.is-uppercase {{link.name | capitalize({onlyFirstLetter: true}) }}
      div.navbar-end
        div.navbar-item
          div(v-for='link in dropdownLinks', :key='link.route')
            nuxt-link.nav-link.buttons(:to='link.route')
              iconstack(:faclass='link.icon')
                span.route {{link.name}}


</template>

<script>
import IconStack from "@/components/IconStack";
// import NavLinks from '@/components/'
// const menu = document.getElementById('navbarSupportedContent')
// const button = document.getElementById('menuButton')
// const dropdown = document.getElementById('navbarDropdown')
// const menu = document.getElementById('navbarSupportedContent')
export default {
  name: "Navbar",
  components: {
    IconStack
  },
  data() {
    return {
      navCollapse: false,
      dropdown: false,
      // signUser: true,
      // logUser: false,
      links: [
        {
          route: "/",
          name: "accueil",
          icon: "fas fa-home"
        },
        // {
        //   route: "/services",
        //   name: "services",
        //   icon: "fas fa-user-tie"
        // },
        {
          route: "/skills",
          name: "compétences",
          icon: "fas fa-user-graduate"
        },
        {
          route: "/portfolio",
          name: "portfolio",
          icon: "fas fa-images"
        },
        {
          route: "/contact",
          name: "contactez-moi",
          icon: "fas fa-envelope"
        },
        {
          route: "/about",
          name: "à propos",
          icon: "fas fa-comment-alt"
        }
      ],
      dropdownLinks: [],
      logs: [
        {
          name: "subscribe",
          color: "btn btn-info",
          name: "Inscription",
          icon: "fas fa-user-plus",
          show: true
        },
        {
          name: "login",
          color: "btn btn-primary",
          name: "Connexion",
          icon: "fas fa-sign-in-alt",
          show: true
        },
        {
          name: "logout",
          color: "btn btn-warning",
          name: "Déconnexion",
          icon: "fas fa-sign-out-alt",
          show: false
        }
      ]
    };
  },
  methods: {
    navbarToggle() {
      this.navCollapse = !this.navCollapse;
    },
    toggleSignUser() {
      this.signUser = !this.signUser;
    },
    toggleLogUser() {
      this.logUser = !this.logUser;
    },
    displayDropdown() {
      this.dropdown = !this.dropdown;
    },

    userbtn() {},
    isActive() {
      this.links = "active";
    },
    brandToHelp() {
      return this.$router.push("/help");
    }
  }
};
</script >

<style >
nav {
  height: 2rem;
  padding: 0.5rem;
}
.navbar-brand {
  text-shadow: 2px 2px 2px grey;
}
.route {
  color: darkslategray;
  text-shadow: 1px 1px 1px grey;
}
</style>
