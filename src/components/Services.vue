<template>
  <section
    id="services"
    class="overflow-hidden"
  >
    <v-row
      class="light"
      no-gutters
    >
      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/assets/Webdesign.jpg')"
          height="100%"
        />
      </v-col>

      <v-col
        class="text-center pa-5"
        cols="12"
        md="6"
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <v-col cols="12">
            <base-bubble-2
              style="transform: translateX(55%)"
            />
            <base-heading class="primary--text">
              Servicios
            </base-heading>
          </v-col>

          <v-col
            v-for="(service, i) in services"
            :key="i"
            class="text-center mb-3"
            md="6"
          >
            <v-avatar
              class="elevation-6 mb-2"
              color="primary"
              size="64"
              tile
            >
              <v-icon
                dark
                size="52"
                v-text="service.icon"
              />
            </v-avatar>

            <base-text>
              <div
                class="mb-2"
                v-text="service.name"
              />
              <div v-html="service.blurb" />
              <div v-text="service.blurb1" />
            </base-text>
          </v-col>
          <v-col cols="12">
            <v-avatar
              class="elevation-5 "
              size="50"
            >
              <v-img
                :src="require('@/assets/Netcore.png')"
              />
            </v-avatar>
            <v-avatar
              class="elevation-5 ml-5"
              size="50"
            >
              <v-img
                :src="require('@/assets/Nodejs.png')"
              />
            </v-avatar>
            <v-avatar
              class="elevation-5 ml-5"
              size="50"
            >
              <v-img
                :src="require('@/assets/Vue.png')"
              />
            </v-avatar>
            <v-avatar
              class="elevation-5 ml-5"
              size="50"
            >
              <v-img
                :src="require('@/assets/Angular.jpg')"
              />
            </v-avatar>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default {
    name: 'Services',

    data: () => ({
      services: [
        {
          name: 'DEVELOPMENT',
          icon: 'mdi-code-tags',
          blurb: 'La innovación y creatividad son los ejes',
          blurb1: 'en el desarrollo de soluciones informáticas.',
        },
        {
          name: 'DESIGN UX',
          icon: 'mdi-pencil-outline',
          blurb: 'Nuestras soluciones se estructuran y diseñan',
          blurb1: 'en función a la experiencia de usuario.',
        },
        {
          name: 'TECHNOLOGIES',
          icon: 'mdi-apps',
          blurb: 'Backend: .NET Core, Node',
          blurb1: 'Frontend: Vue, Angular.',
        },
        {
          name: 'SUPPORT',
          icon: 'mdi-account',
          blurb: 'Soporte técnico 24/7 con',
          blurb1: 'profesionales y técnicos capacitados.',
        },
      ],
    }),
  }
</script>
