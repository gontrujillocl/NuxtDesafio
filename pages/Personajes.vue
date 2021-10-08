<template>
  <div class="mt-2">
    <v-row>
      <v-col></v-col>
      <v-col align="center" cols="3">
        <h1>Personajes</h1>
      </v-col>
      <v-col></v-col>
    </v-row>
    <v-row>
      <v-col v-for="personaje in personajes" :key="personaje.id" xl="4">
        <v-card class="rounded-xl">
          <v-img class="mx-auto rounded-xl" :src="personaje.imagen" width="200px" />
          <v-card-title class="justify-center">{{
            personaje.nombre
          }}</v-card-title>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  computed: {
    personajes() {
      return this.$store.state.personajeModule.personajes
    },
  },
}
</script>


