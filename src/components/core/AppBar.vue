<template>
  <v-app-bar
    v-scroll="onScroll"
    :color="!isScrolling ? 'transparent' : 'secondary'"
    fixed
    flat
  >
    <v-slide-x-transition>
      <v-img
        v-if="showLogo"
        :src="require('@/assets/Logo1.png')"
        class="shrink"
        contain
        max-height="35"
      />
    </v-slide-x-transition>
    <v-slide-x-transition>
      <tr
        v-if="showLogo"
        id="formatoLogo"
        class="primary--text hidden-sm-and-down"
      >
        Cafe<b id="formatoand" class="font-weight-thin ml-1 mr-1 font-italic">&</b>Tech
      </tr>
    </v-slide-x-transition>
    <v-spacer />
    <v-slide-x-transition>
      <tr
        v-if="showLogo"
        id="formatoSlogan"
        class="primary--text hidden-sm-and-down"
      >
        Technology Applications for Business
      </tr>
    </v-slide-x-transition>

    <v-spacer />
    <!-- <social-media
      v-if="showLogo"
      class="hidden-sm-and-down"
    /> -->

    <div class="text-center"><!-- https://decafeapp.decafeymas.com/ -->
      <v-btn
        v-if="showLogo"
        id="formatoApp"
        class="ml-3 white--text floating-sm-left font-weight-thin"
        medium
        rounded
        color="primary"
        href="http://www.decafeytech.com/"
        target="blank"
      >
      ERP Decafeapp

        <v-icon
          right
          medium
        >
          mdi-apps
        </v-icon>
      </v-btn>
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
#formatoand  {
    font-family:Helvetica;
    font-size: 1.5rem;
}
#formatoLogo {
    font-family: 'Mina', sans-serif;
    font-size: 1.8rem;
    margin-left: -5.5%;
    margin-top: 0.8%;
}
#formatoSlogan  {
    font-family: 'Mina', sans-serif;
    font-size: 1.2rem;
}
#formatoApp {
    font-family: 'Mina', sans-serif;
    font-size: 1rem;
}
</style>
