<template lang="pug">
  div.box.is-warning.container
      div
        img.float-left(src='https://cdn.pixabay.com/photo/2013/04/01/10/55/attention-98643_960_720.png', alt='image attention')
        h1.title.text-center Oops!
        h2.text-center Problème de rendu... désolé!
      .text-right.w-75
        nuxt-link(to='/') Retour à l'accueil

</template>

<style scoped>
  img {
    width: 8rem;
  }

</style>

