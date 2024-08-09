<template>
  <v-container>
    <!-- Welcome Section -->
    <v-row class="mb-5" justify="center">
      <v-col cols="12" md="8">
        <v-card class="elevation-12">
          <v-card-title class="headline">
            Welcome to My Portfolio!
          </v-card-title>
          <v-card-text>
            <p>I'm Jonathan Andres Pardo, a passionate software engineer specializing in automation and software development.</p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <!-- Projects Section -->
    <v-row class="mb-5">
      <v-col cols="12">
        <v-card class="elevation-12">
          <v-card-title class="headline">Featured Projects</v-card-title>
          <v-card-text>
            <v-row>

              <!-- Demoblaze Serenity Project -->
              <v-col cols="12" md="4" sm="6">
                <v-card class="pa-4">
                  <v-card-title>Demoblaze Serenity Project</v-card-title>
                  <v-card-subtitle>Serenity BDD with Java</v-card-subtitle>
                  <v-card-text>
                    <p>This project uses Serenity BDD with Java 17 and Maven to automate tests on the demoblaze.com page. The project includes the following use cases:</p>
                    <ul>
                      <li>Registering a new user on the Product Store page.</li>
                      <li>Making a purchase by adding products to the cart.</li>
                    </ul>
                    <p><strong>Prerequisites:</strong></p>
                    <ul>
                      <li>JDK 17</li>
                      <li>Maven 3.6.3 or above</li>
                    </ul>
                    <p><strong>Environment Configuration:</strong></p>
                    <p>Specify the browser to use via the -Denvironment property in Maven commands:</p>
                    <ul>
                      <li>Chrome: <code>mvn clean verify -Denvironment=chrome</code></li>
                      <li>Firefox: <code>mvn clean verify -Denvironment=firefox</code></li>
                    </ul>
                    <p><strong>Project Structure:</strong></p>
                    <pre>
├── test
│   ├── java
│   │   ├── demoblaze
│   │   │   ├── questions
│   │   │   ├── runners
│   │   │   ├── stepdefinitions
│   │   │   ├── task
│   │   │   ├── userinterfaces
├── resources
│   ├── features
│   ├── junit-platform.properties
│   ├── logback-test.xml
│   ├── serenity.conf
├── pom.xml
                    </pre>
                    <p>Integrates Screenplay pattern using Cucumber.</p>
                    <p><strong>Continuous Integration:</strong></p>
                    <p>Automatically generates reports using GitHub Actions. Any changes trigger tests at:</p>
                    <a href="https://stormtrooper96.github.io/demoblazeJonathanandresPardo/" target="_blank">Project Reports</a>
                    <p>Action can be executed via:</p>
                    <a href="https://github.com/stormtrooper96/demoblazeJonathanandresPardo/actions/workflows/living-documentation.yml" target="_blank">GitHub Actions Workflow</a>
                  </v-card-text>
                  <v-card-actions>
                    <v-btn color="primary" @click="openLink('https://github.com/stormtrooper96/demoblazeJonathanandresPardo')">View Project</v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>
              <!-- Kantanekov2 API Project -->
              <v-col cols="12" md="4" sm="6">
                <v-card class="pa-4">
                  <v-card-title>Kantanekov2 API</v-card-title>
                  <v-card-subtitle>Spring Boot API</v-card-subtitle>
                  <v-card-text>
                    <p>This project includes an API built with Spring Boot for a veterinary system. Key classes include:</p>
                    <ul>
                      <li>AforegoingService</li>
                      <li>AnimalTypeService</li>
                      <li>AppointmentService</li>
                      <li>AuthenticationService</li>
                      <li>CompanyService</li>
                      <li>ConsultoryService</li>
                      <li>EmployeeService</li>
                      <li>PetService</li>
                      <li>UserRoleService</li>
                      <li>VeterinaryService</li>
                    </ul>
                    <p><strong>Repository:</strong></p>
                    <a href="https://github.com/stormtrooper96/kantanekov2Api/tree/master" target="_blank">View Repository</a>
                  </v-card-text>
                  <v-card-actions>
                    <v-btn color="primary" @click="openLink('https://github.com/stormtrooper96/kantanekov2Api/tree/master')">View Project</v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <!-- Skills Section -->
    <v-row class="mb-5">
      <v-col cols="12">
        <v-card class="elevation-12">
          <v-card-title class="headline">Technical Skills</v-card-title>
          <v-card-text>
            <v-row>
              <v-col cols="12" lg="4" md="6">
                <v-chip class="ma-2" color="blue" light>
                  Java
                </v-chip>
              </v-col>
              <v-col cols="12" lg="4" md="6">
                <v-chip class="ma-2" color="green" light>
                  Selenium
                </v-chip>
              </v-col>
              <v-col cols="12" lg="4" md="6">
                <v-chip class="ma-2" color="orange" light>
                  Vue.js
                </v-chip>
              </v-col>
              <v-col cols="12" lg="4" md="6">
                <v-chip class="ma-2" color="red" light>
                  Node.js
                </v-chip>
              </v-col>
              <v-col cols="12" lg="4" md="6">
                <v-chip class="ma-2" color="purple" light>
                  MongoDB
                </v-chip>
              </v-col>
              <v-col cols="12" lg="4" md="6">
                <v-chip class="ma-2" color="teal" light>
                  Jenkins
                </v-chip>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <!-- Certifications Section -->
    <v-row class="mb-5">
      <v-col cols="12">
        <v-card class="elevation-12">
          <v-card-title class="headline">Certifications</v-card-title>
          <v-card-text>
            <v-chip class="ma-2" color="primary" light>
              Scrum Master
            </v-chip>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'Home',
    methods: {
      openLink (url) {
        window.open(url, '_blank')
      },
    },
  }
</script>
