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
        <v-img
          contain
          :src="require('@/assets/Decafe222.png')"
          class="grow hidden-sm-and-down ml-5 mt-5"
          max-height="80"
          width="100%"
          position="top left"
        />
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