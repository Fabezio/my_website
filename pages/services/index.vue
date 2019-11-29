<template lang="pug">
  #services
    h1.text-center.mb-4.header-shadow Services
    .card-deck.my-4
      .card.silver-shadow(v-for='service in services', :key='service.id')
        h2.card-header {{service.title}}
        .card-body
          p.card-text.text-justify {{service.paragraph}}
    .row.my-5
      .col-md-12
        a.btn.btn-lg.btn-block.btn-primary.text-light.btn-shadow(href='#') Oui, je demande une création/amélioration de site web

</template>

<script>
export default {
  name: "Services",
  data: () => {
    return {
      services: [
        {
          id: "create",
          title: "Création",
          paragraph:
            "Besoin d'un site web? Vous êtes au bon endroit. Tout sera fait pour répondre à vos besoins."
        },
        {
          id: "adapt",
          title: "Adaptation",
          paragraph:
            "Si votre site manque de réactivité ou est mal supporté par les navigateurs, alors il est urgent de le remettre au goût du jour."
        },
        {
          id: "optimize",
          title: "Optimisation",
          paragraph:
            "Vous avez un site web mais il ne s'affiche pas correctement sur votre smartphone ou tablette? Rendez-le responsive! De cette façon, vous l'adapterez à tous les supports numériques, fixes ou mobiles, et même pour les écrans TV!"
        }
      ]
    };
  }
  /*

    */
};
</script>

<style scoped>
.carousel-control-prev-icon,
.carousel-control-next-icon {
  background: rgba(0, 0, 0, 0.5);
  color: white;
}

.carousel-caption {
  background: rgba(0, 0, 0, 0.5);
  border-radius: 5px 5px 0 0;
  /*
  */
}
.carousel-indicators {
  width: 1rem;
  height: 1rem;
}
</style>
