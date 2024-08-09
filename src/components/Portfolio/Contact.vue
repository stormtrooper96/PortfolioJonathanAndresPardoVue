<template>
  <v-container>
    <v-row justify="center">
      <v-col cols="12" md="8">
        <v-card>
          <v-card-title class="headline">
            Contact Me
          </v-card-title>
          <v-card-text>
            <v-form>
              <v-text-field label="Name" required></v-text-field>
              <v-text-field label="Email" required></v-text-field>
              <v-textarea label="Message" required></v-textarea>
              <v-btn color="primary" @click="sendMessage">Send</v-btn>
            </v-form>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Contact',
  methods: {
    sendMessage() {
      alert('Message sent!');
    },
  },
};
</script>
