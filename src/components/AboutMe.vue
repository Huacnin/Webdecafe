<template>
  <section
    id="about"
    class="overflow-hidden"
  >
    <v-row
      class="primary"
      no-gutters
    >
      <v-col
        class="pa-5"
        cols="12"
        md="6"
      >
        <base-bubble-1 style="transform: translate(10%, -5%)" />

        <base-heading class="white--text">
          Equipo Humano
        </base-heading>

        <base-text class="mb-5 success--text">
          Contamos con un staff de profesionales y técnicos<br>
          altamente calificados, capacitados y certificados en <br>
          las tecnologias y plataformas de desarrollo de mayor demanda.
        </base-text>

        <base-subheading class="white--text">
          Experiencias & Habilidades
        </base-subheading>

        <v-alert
          outlined
          color="secondary"
        >
          <v-row
            v-for="(skill, i) in skills"
            :key="i"
            style="color: info;"
          >
            <v-col
              class="text-uppercase"
              cols="6"
              v-text="skill.name"
            />

            <v-col
              class="text-right"
              cols="6"
              v-text="`${skill.value}%`"
            />

            <v-progress-linear
              :value="skill.value"
              color="accent"
              height="8"
            />
          </v-row>
        </v-alert>
      </v-col>

      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/assets/Equipo.jpg')"
          height="100%"
        />
      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default {
    data: () => ({
      skills: [
        {
          name: 'Web Design ',
          value: 85,
        },
        {
          name: 'Mobile apps',
          value: 80,
        },
        {
          name: 'Web Development ',
          value: 90,
        },
        {
          name: 'Marketing & Communications',
          value: 90,
        },
      ],
    }),
  }
</script>
