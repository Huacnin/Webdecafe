<template>
  <section
    id="welcome"
    class="overflow-hidden"
  >
    <v-row no-gutters>
      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/assets/ti.jpg')"
          height="117vh"
        />
      </v-col>

      <v-col
        class="align-content-space-between layout wrap"
        cols="12"
        md="6"
      >
      <div class="text-center">
        <v-img
          contain
          :src="require('@/assets/Logo1.png')"
          class="grow hidden-sm-and-down mt-7"
          max-height="45"
          width="100%"
        />
        <p id="formatoLogo" class="font-weight-thin"> Decafe<b id="formatoand" class="font-weight-thin ml-1 mr-1 font-italic">&</b>Tech</p> 
        <p id="formatoSlogan" class="accent--text font-weight-thin">Technology Applications for Business</p> 
        </div>
        <v-row
          align="center"
          justify="center"
        >
          <v-col
            cols="12"
            md="6"
          >
            <base-heading class="mt-15 text-center">
              Bienvenidos!
            </base-heading>
            <base-text class=" pl-5 mr-5 mt-10 text-justify">
              Somos una consultora  que  diseña, desarrolla y  provisiona  soluciones
              tecnológicas  que  ayudan  a las empresas  a transformarse digitalmente
              generando la automatización de sus procesos de gestión y fortaleciendo su
              relacion comercial con sus clientes y proveedores. <br>
              El code del diseño y desarrollo  de nuestras soluciones tecnológicas se
              basan  en  la experiencia de usuario, la  innovacion  y  creatividad lo
              que nos permite ofrecer  soluciones que se adapten a los requerimientos
              y necesidades de nuestros clientes.
            </base-text>
          </v-col>
        </v-row>
        <v-img
          contain
          :src="require('@/assets/Tech.jpg')"
          class="grow hidden-sm-and-down mb-5"
          max-height="175"
          width="100%"
          position="top right"
          style="transform: rotate(180deg) translateX(-74%)"
        />
      </v-col>
    </v-row>
  </section>
</template>
<style scoped>
#formatoand {
    font-family:Helvetica;
    font-size: 1.5rem;
}
#formatoLogo {
    font-family: 'Mina', sans-serif;
    font-size: 2rem;
    margin-top: 3%;
}
#formatoSlogan {
    font-family: 'Mina', sans-serif;
    font-size: 0.7rem;
    margin-top: -9%;
}
</style>