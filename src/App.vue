<template>
  <v-app>
    <!-- Barra de Aplicación -->
    <v-app-bar color="primary" density="compact">
      <template #prepend>
        <!-- Icono de navegación para pantallas pequeñas -->
        <v-app-bar-nav-icon class="d-sm-none" @click="drawer = !drawer" />
      </template>

      <v-app-bar-title>Photos</v-app-bar-title>

      <template #append>
        <!-- Botones de navegación en la barra de aplicaciones para pantallas grandes -->

        <v-btn class="d-none d-md-flex" @click="navigateTo('/')">Home</v-btn>
        <v-btn class="d-none d-md-flex" @click="navigateTo('/about')">About</v-btn>
        <v-btn class="d-none d-md-flex" @click="navigateTo('/cv')">CV</v-btn>

        <v-btn class="d-none d-md-flex" @click="navigateTo('/contact')">Contact</v-btn>
      </template>
    </v-app-bar>

    <!-- Panel de Navegación Lateral para pantallas pequeñas -->
    <v-navigation-drawer v-model="drawer" absolute class="d-sm-block d-md-none" temporary>
      <v-list dense nav>
      <v-list-item-group>
        <v-list-item v-for="(item, index) in items" :key="index" @click="navigateTo(item.route)">
          <v-list-item-title>{{ item.name }}</v-list-item-title>
        </v-list-item>
      </v-list-item-group>
    </v-list>
    </v-navigation-drawer>
    <v-main>

      <router-view />
    </v-main>
  </v-app>
</template>

<script>
  export default {
    name: 'App',
    data () {
      return {
        drawer: false,
        tab: 0,
        items: [
          { name: 'Home', route: '/' },
          { name: 'About', route: '/about' },
          { name: 'Cv', route: '/cv' },
          { name: 'Contact', route: '/contact' },

        ],
      }
    },
    methods: {
      navigateTo (route) {
        this.$router.push(route)
        this.drawer = false // Cerrar el panel de navegación en pantallas pequeñas después de la selección
      },
    },
  }
</script>

<style scoped>
/* Estilos específicos para este componente */
</style>
