<template>
  <v-footer app height="auto">
    <v-container class="py-2" fluid>
      <v-row justify="center">
        <v-col class="text-center" cols="12">
          <a
            class="social-link"
            href="https://www.linkedin.com/in/japardos/"
            rel="noopener noreferrer"
            target="_blank"
            title="LinkedIn"
          >
            <v-icon size="24">mdi-linkedin</v-icon>
          </a>
          <p class="text-caption mt-2">
            &copy; {{ (new Date()).getFullYear() }} Jonathan Andrés Pardo
          </p>
        </v-col>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script setup lang="ts">
// No se necesita código adicional para esta configuración básica
</script>

<style scoped lang="sass">
.social-link
  color: #0077b5 // LinkedIn color
  text-decoration: none
  transition: color 0.2s ease-in-out

  &:hover
    color: #005582 // Darker shade on hover

.v-footer
  background-color: #1e1e1e
  color: #e0e0e0
</style>
