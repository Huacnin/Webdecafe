<template>
  <v-footer
    height="60"
    class="justify-center"
  >
    <v-container>
      <v-row
        align="center"
        no-gutters
      >
        <v-col
          cols="12"
          sm="6"
          md="4"
        >
          <div class="text-left">
            &copy;{{ new Date().getFullYear() }}
          </div>
        </v-col>
        <v-spacer />
        <v-col
          cols="12"
          sm="6"
          md="4"
        >
          <div
            id="formatoLogo"
            class="text-center font-weight-light"
          >
            Decafe & Más
          </div>
        </v-col>
        <v-col
          cols="12"
          sm="6"
          md="4"
        >
          <div class="font-weight-thin pt-6 pt-md-0 text-right">
            Made with
            <v-icon
              size="18"
              color="primary"
            >
              mdi-heart
            </v-icon>
            by <a
              class="primary--text text-decoration-none"
              href="https://www.decafeymas.somee.com"
            >Decafe & Más S.A.C.</a>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
  export default {
    name: 'CoreFooter',

    components: {
      // SocialMedia: () => import('@/components/SocialMedia'),
    },
  }
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css?family=Helvetica');
@import url('https://fonts.googleapis.com/css?family=Mina');
#formatoWhatsapp  {
    font-family:Arial, Helvetica, sans-serif;
    font-size: 1.3rem;
}
#formatoLogo {
    font-family: 'Mina';
    font-size: 1rem;
    margin-top: 1%;
}
</style>
