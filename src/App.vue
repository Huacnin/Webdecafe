<template>
  <v-app v-scroll="onScroll">
    <core-app-bar/>
    <core-view/>
    <v-btn
      id="flotanteWhats"
      rounded
      large
      class="text-capitalize white--text  font-weight-medium"
      href="https://wa.me/51964023536?text=Me%20interesa%20conocer%20más%20sobre%20sus%20aplicaciones"
      target="blank"
      >
      <v-img
        contain
        width="32"
        :src="require('@/assets/Whatsapp.png')"
        class="mr-3"
      />
      WhatsApp
    </v-btn>
    <v-fab-transition>
      <v-btn
        v-if="showButtom"
        class="button-up"
        fab
        outlined
        large
        color="success"
        @click="scrollUp()"
      >
        <v-icon
          medium
          color="primary"
        >
          mdi-chevron-up
        </v-icon>
      </v-btn>
    </v-fab-transition>    
    <core-footer/>
  </v-app>
</template>

<script>
  export default {
    name: 'App',

    components: {
      CoreAppBar: () => import('@/components/core/AppBar'),
      CoreFooter: () => import('@/components/core/Footer'),
      CoreView: () => import('@/components/core/View'),
    },
    data: () => ({
      showButtom: false,
      fab: false,
    }),

    methods: {
      onScroll () {
        const offset = window.pageYOffset
        this.showButtom = offset > 500
      },
      scrollUp () {
        const currentScroll = document.documentElement.scrollTop
        if (currentScroll > 0) {
          window.requestAnimationFrame(this.scrollUp)
          window.scrollTo(0, currentScroll - (currentScroll / 10))
        }
      },
    },
  }
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css?family=Helvetica');
#flotanteWhats{
    display:scroll;
    position:fixed;
    bottom:160px;
    left:30px;
    font-family:Arial, Helvetica, sanSs-serif;
    font-size: 1.3rem;
    background-color: #455A64;
}
.button-up {
  display:scroll;
  position: fixed;
  right: 40px;
  bottom:160px;
  background-color: #f0f0f0;
  border-color: #ffffff;
  transition: 0.1s ease;
}
.button-up:hover{
  transform:scale(1.12);
  border-color:6px #455A64;
  border-bottom-color: #ffffff ;
  border-top-color: #ffffff;
  border-right-color: #ffffff;
  border-left-color: #ffffff;
}
</style>