<template lang="pug">
 #portfolio
  h1.text-center.mb-4.header-shadow Portfolio
  article
    h2.header-shadow.mb-3 Sites créés en formation:
    .card-deck
      .card.silver-shadow.text-center(v-for='creation in creations', :key='creation.mod')
        img.card-img-top(data-toggle='modal', :data-target="'#' + creation.mod", :src='creation.img', :alt='creation.alt')
        .card-body
          h3.card-title.text-uppercase {{creation.name}}
          p.card-text.display-5 {{creation.desc}}
        .card-footer.mb-0
          a.btn.btn-outline-link.display-5.text-uppercase(:href="'https://' + creation.url", target='_blank')
            i.fas.fa-sign-in-alt
            | Consulter
    .modal.collapse.fade(v-for='creation in creations', :key='creation.mod', :id='creation.mod')
      .modal-dialog.modal-md
        .modal-content
          .modal-header
            h4 {{creation.name}}
            button.close(data-dismiss='modal') ×
          .modal-body
            img.w-100(:src='creation.img')
          .modal-footer
            .btn-group.btn-lg.btn-rounded
              button.btn.btn-dark(data-dismiss='modal')
                i.mr-1.far.fa-window-close.text-danger.text-light
                |  Annuler
              a.btn.btn-success(:href="'https://' + creation.url", target='_blank')
                i.mr-1.fas.fa-sign-in-alt
                |  Aller
</template>

<script>
export default {
  name: "",
  data() {
    return {
      path: "~/assets/img/portfolio",
      creations: [
        {
          url: "voyages.fabezio.com",
          img: "https://cv.fabezio.com/img/voyage.png",
          mod: "voyage",
          alt: "photo du site",
          name: "Travel Agency",
          desc: "Premier site en HTML / CSS"
        },
        {
          url: "snake.fabezio.com",
          img: "http://cv.fabezio.com/img/snake-maj.png",
          mod: "snake",
          alt: "photo du site",
          name: "Snakey",
          desc: "Version JS de Snake"
        },
        {
          url: "actrices.fabezio.com",
          img: "http://cv.fabezio.com/img/actrices.png",
          alt: "photo du site",
          mod: "actrices",
          name: "Top 5 Actrices",
          desc: "Site en jQuery"
        }
      ]
    };
  }
  /*

    */
};
</script>

<style scoped>
#portfolio .card img {
  filter: grayscale(100%);
  opacity: 0.75;
}
#portfolio .card img:hover {
  filter: grayscale(0%);
  opacity: 1;
}
.card-body {
  border-top: aquamarine 1.5px solid;
}
</style>
