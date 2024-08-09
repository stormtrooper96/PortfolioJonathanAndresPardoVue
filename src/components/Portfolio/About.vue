<template>
  <v-container class="about-me">
    <!-- Profile Section -->
    <v-row align="center" class="mb-10" justify="center">
      <v-col class="text-center" cols="12" md="4">
        <v-avatar size="150">
          <v-img
            alt="Jonathan Andrés Pardo"
            class="profile-picture"
            src="@/assets/profile-picture.jpeg"
          />
        </v-avatar>
        <h2 class="mt-4">Jonathan Andrés Pardo</h2>
        <p class="subtitle">QA Automation Expert & Scrum Master</p>
      </v-col>
    </v-row>

    <!-- Intro Section -->
    <v-row>
      <v-col cols="12">
        <v-card class="pa-6" elevation="4">
          <v-card-title class="headline">Who Am I?</v-card-title>
          <v-card-text class="about-me-text">
            I'm Jonathan Andrés Pardo, a System Engineer with over 5 years of experience in QA automation. When I'm not crafting automated test scripts, you’ll find me exploring new trails, jamming to classic rock, or diving into the latest video game.
          </v-card-text>
          <v-divider class="my-4" />
          <v-card-subtitle class="text-h5 mb-3">Hobbies & Interests</v-card-subtitle>
          <v-row>
            <v-col cols="12" md="4">
              <v-icon color="cyan lighten-4" large>mdi-guitar-electric</v-icon>
              <p>Rock Music Enthusiast</p>
              <v-chip class="ma-1" color="cyan lighten-4" dark>Classic Rock</v-chip>
              <v-chip class="ma-1" color="cyan lighten-4" dark>Power Metal</v-chip>
              <v-chip class="ma-1" color="cyan lighten-4" dark>Thrash Metal</v-chip>
            </v-col>
            <v-col cols="12" md="4">
              <v-icon color="lime lighten-4" large>mdi-controller-classic</v-icon>
              <p>Video Gamer</p>
              <v-chip class="ma-1" color="lime lighten-4" dark>RPGs</v-chip>
              <v-chip class="ma-1" color="lime lighten-4" dark>Action</v-chip>
            </v-col>
            <v-col cols="12" md="4">
              <v-icon color="amber lighten-4" large>mdi-hiking</v-icon>
              <p>Hiking & Adventure</p>
              <v-chip class="ma-1" color="amber lighten-4" dark>Mountain Trails</v-chip>
              <v-chip class="ma-1" color="amber lighten-4" dark>Nature Parks</v-chip>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>

    <!-- Professional Section -->
    <v-row class="mt-10">
      <v-col>
        <v-card class="pa-6" elevation="4">
          <v-card-title class="headline">Professional Expertise</v-card-title>
          <v-list dense>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>
                  <strong>Automation and Testing:</strong> Proficient in crafting automated test scripts using Java, Selenium, Appium, and RestAssured.
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>
                  <strong>Continuous Integration/Continuous Delivery (CI/CD):</strong> Expert in implementing CI/CD pipelines using Jenkins, Docker, and Git.
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title>
                  <strong>Agile Methodologies:</strong> Lead teams with an agile mindset, fostering collaboration and continuous improvement in the software development lifecycle.
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'AboutMe',
}
</script>

<style scoped>
.about-me {
  background-color: #121212;
  color: #e0e0e0;
  padding: 20px;
}

.profile-picture {
  border-radius: 50%;
  border: 4px solid #1e88e5;
}

.subtitle {
  font-size: 1.2rem;
  color: #b0bec5;
}

.about-me-text {
  font-size: 1.1rem;
  line-height: 1.6;
  color: #e0e0e0;
}

.headline {
  font-weight: bold;
  color: #1e88e5;
}

.v-icon {
  font-size: 40px;
}

v-chip {
  font-size: 0.8rem;
}

.v-divider {
  margin-top: 16px;
  margin-bottom: 16px;
}
</style>
