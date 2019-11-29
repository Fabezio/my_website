<template lang="pug">
  div
    h1.title.text-center Contactez-moi!
    form(action='', @submit.prevent='sendForm')
      .input-group.mb-3
        .input-group-prepend
          span#basic-addon1.input-group-text.far.fa-user
        input#lastname.form-control(type='text', placeholder='Nom', aria-label='Nom', aria-describedby='basic-addon1')
      .input-group.mb-3
        .input-group-prepend
          span#basic-addon1.input-group-text.far.fa-user
        input#firstname.form-control(type='text', placeholder='Prénom', aria-label='Prénom', aria-describedby='basic-addon1')
      .input-group.mb-3
        .input-group-prepend
          span#basic-addon1.input-group-text.far.fa-building
        input#society.form-control(type='text', placeholder='Entreprise', aria-label='Enreprise', aria-describedby='basic-addon1')

      .input-group.mb-3
        .input-group-prepend
          span#basic-addon1.input-group-text.far.fa-envelope
        input#email.form-control(type='email', placeholder='Email', aria-label='Email', aria-describedby='basic-addon1')
      .input-group.mb-3
        .input-group-prepend
          span#basic-addon1.input-group-text.far.fa-comment-dots
        textarea#message.form-control(type='email', placeholder='Message', rows='3', aria-label='Message', aria-describedby='basic-addon1')
    
</template>
