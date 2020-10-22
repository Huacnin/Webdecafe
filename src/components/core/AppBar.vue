<template>
  <v-app-bar
    v-scroll="onScroll"
    :color="!isScrolling ? 'transparent' : 'white'"
    fixed
    flat
  >
    <v-slide-x-transition>
      <v-img
        v-if="showLogo"
        :src="require('@/assets/Decafe2222.png')"
        class="shrink"
        contain
        max-height="55"
      />
    </v-slide-x-transition>
    <v-slide-x-transition>
      <tr
        v-if="showLogo"
        id="formatoLogo"
        class="text-capitalize primary--text hidden-sm-and-down"
      >
        Decafe & Más
      </tr>
    </v-slide-x-transition>
    <v-spacer />
    <v-slide-x-transition>
      <tr
        v-if="showLogo"
        id="formatoSlogan"
        class="primary--text hidden-sm-and-down"
      >
        Tecnologías para el éxito de su negocio.
      </tr>
    </v-slide-x-transition>

    <v-spacer />
    <!-- <social-media
      v-if="showLogo"
      class="hidden-sm-and-down"
    /> -->

    <div class="text-center">
      <base-btn
        v-if="showLogo"
        id="formatoSlogan"
        class="ml-3 white--text floating-sm-left"
        medium
        href="https://decafeapp.decafeymas.com"
        target="blank"
      >
        ERP Decafeapp

        <v-icon
          right
          medium
        >
          mdi-apps
        </v-icon>
      </base-btn>
    </div>
  </v-app-bar>
</template>

<script>
  export default {
    name: 'CoreAppBar',

    components: {
      // SocialMedia: () => import('@/components/SocialMedia'),
    },

    data: () => ({
      showLogo: false,
      isScrolling: false,
    }),

    methods: {
      onScroll () {
        const offset = window.pageYOffset
        this.isScrolling = offset > 50
        this.showLogo = offset > 100
      },
    },
  }
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css?family=Mina');

#formatoLogo {
    font-family: 'Mina';
    font-size: 2.1rem;
    margin-left: -3%;
    margin-top: 0.4%;
}
#formatoSlogan  {
    font-family: 'Mina';
    font-size: 1.2rem;
}
</style>
