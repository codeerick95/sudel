<template>
  <section class="banner-contact text-white" v-bind:style="{ backgroundImage: 'url(' + bg + ')' }">
    <div class="banner-contact__bg-dark">
      <div class="container">
        <div class="row align-items-center">

          <div class="col-md-5 col-lg-6 d-flex justify-content-center mb-3 mb-md-0">
            <img src="https://administrador.sudel.com.pe/wp-content/uploads/2020/06/SUDEL-LOGO.png" alt="" class="banner-contact__image">
          </div>

          <div class="col-md-7 col-lg-6 text-center text-md-left">
            <h2 class="banner-contact__title mb-3">¿Tienes dudas?</h2>

            <h3 class="banner-contact__subtitle">
              CONVERSA CON UN ASESOR COMERCIAL
            </h3>

            <p class="lead text-warning">Estaremos gustosos de atenderte.</p>

            <a :href="`https://api.whatsapp.com/send?phone=+51${info.whatsapp}`" target="_blank" class="btn btn-success">
              <i class="fab fa-whatsapp"></i>
              Contacta con un asesor vía Whatsapp</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    data() {
      return {
      }
    },
    props: ['info', 'bg']
  }
</script>

<style lang="scss">
  @import "../../scss/variables";

.banner-contact {
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;

  &__bg-dark {
    width: 100%;
    height: 100%;

    background-color: rgba($dark, .9);

    padding: 3em;

    @media (min-width: 1024px) {
      padding: 5em 0;
    }
  }

  &__title {
    font-size: 1.5em;
    font-weight: 800;

    @media (min-width: 1024px) {
      font-size: 2.5em;
    }
  }

  &__subtitle {
    font-size: 1.1em;
    font-weight: 800;
  }

  &__image {
    max-width: 30%;
  }
}
</style>
