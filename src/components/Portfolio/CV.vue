<template>
  <v-container class="pa-4" fluid>
    <!-- Header Section -->
    <v-row align="center" class="mb-5 header-section" justify="center">
      <v-col class="text-center" cols="12">
        <h1 class="display-2">Curriculum Vitae</h1>
        <p class="headline">Jonathan Andrés Pardo</p>
      </v-col>
    </v-row>

    <!-- Profile Section -->
    <v-row align="center" class="mb-5" justify="center">
      <v-col class="text-center" cols="12" md="4">
        <v-avatar class="mx-auto profile-picture" size="120">
          <v-img
            alt="Jonathan Andrés Pardo"
            src="@/assets/profile-picture.jpeg"
          />
        </v-avatar>
        <h2 class="mt-3 text-h5">Jonathan Andrés Pardo</h2>
        <p class="subtitle">QA Automation Expert & Scrum Master</p>
        <v-btn class="mt-3" color="primary" large>Download CV</v-btn>
      </v-col>
    </v-row>

    <!-- Experience Section -->
    <v-row>
      <v-col cols="12">
        <v-card class="pa-4 mb-5" elevation="2">
          <v-card-title class="headline">Professional Experience</v-card-title>
          <v-timeline align-top>
            <v-timeline-item
              v-for="(item, index) in experience"
              :key="index"
              class="timeline-item"
              :color="item.color"
              :icon="item.icon"
              small
            >
              <v-card class="timeline-card">
                <v-card-title>{{ item.title }}</v-card-title>
                <v-card-subtitle>{{ item.company }} | {{ item.period }}</v-card-subtitle>
                <v-card-text>{{ item.description }}</v-card-text>
              </v-card>
            </v-timeline-item>
          </v-timeline>
        </v-card>
      </v-col>
    </v-row>

    <!-- Education Section -->
    <v-row>
      <v-col cols="12">
        <v-card class="pa-4 mb-5" elevation="2">
          <v-card-title class="headline">Education</v-card-title>
          <v-list dense>
            <v-list-item v-for="(edu, index) in education" :key="index">
              <v-list-item-content>
                <v-list-item-title><strong>{{ edu.degree }}</strong></v-list-item-title>
                <v-list-item-subtitle>{{ edu.institution }} | {{ edu.period }}</v-list-item-subtitle>
                <v-list-item-text>{{ edu.description }}</v-list-item-text>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
    </v-row>

    <!-- Skills Section -->
    <v-row>
      <v-col cols="12">
        <v-card class="pa-4 mb-5" elevation="2">
          <v-card-title class="headline">Skills</v-card-title>
          <v-row>
            <v-col v-for="(skill, index) in skills" :key="index" cols="12" sm="6">
              <v-progress-linear
                class="mb-4"
                color="primary"
                height="20"
                :value="skill.value"
              >
                <span class="progress-value">{{ skill.value }}%</span>
                <strong>{{ skill.name }}</strong>
              </v-progress-linear>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>

    <!-- Languages Section -->
    <v-row>
      <v-col cols="12">
        <v-card class="pa-4" elevation="2">
          <v-card-title class="headline">Languages</v-card-title>
          <v-row>
            <v-col v-for="(language, index) in languages" :key="index" cols="12" sm="4">
              <v-chip class="ma-2" color="primary" light>
                {{ language.name }} - {{ language.level }}
              </v-chip>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Cv',
  data() {
    return {
      experience: [
        {
          title: 'QA Automation Engineer',
          company: 'Neoris S.A.S',
          period: '2024-Actual',
          description: 'Developing automated test scripts using Selenium, Appium, and RestAssured. Leveraging AWS services such as Lambdas, Step Functions, CloudWatch, and API Gateways for application monitoring and performance validation. Conducting performance, load, and stress testing with JMeter. Expertise in SQL for data validation and using Git for source code management.',
          color: 'blue',
          icon: 'mdi-briefcase',
        },
        {
          title: 'Quality Assurance Engineer',
          company: 'Inter Rapidisimo S.A.',
          period: 'September 2022 - May 2024',
          description: 'Constructed test scripts, certified production steps, created and executed test plans, designed test cases, and documented both functional and non-functional tests. Implemented and executed tests in AWS, using Lambdas, Step Functions, CloudWatch, and API Gateways. Performed performance, load, and stress testing using JMeter. Developed automated test scripts with Java, Selenium, Appium, RestAssured, and Serenity. Validated data accuracy with SQL queries and managed code repositories with GIT.',
          color: 'green',
          icon: 'mdi-cogs',
        },
        {
          title: 'QA Automation Analyst',
          company: 'ConexRed S.A.',
          period: 'August 2021 - August 2022',
          description: 'Performed performance, load, and stress testing using JMeter to detect memory leaks and other issues. Created test scripts, certified production steps, developed test plans, and documented both functional and non-functional tests. Implemented continuous integration practices using Jenkins, Docker, and Selenium Grid for automated build and deployment. Developed automated test scripts using Java, Selenium, Appium, RestAssured, and Serenity. Validated data with SQL queries and managed code repositories with GIT.',
          color: 'orange',
          icon: 'mdi-cogs',
        },
        {
          title: 'QA Analyst',
          company: 'Cizaro S.A.S',
          period: 'November 2018 - July 2021',
          description: 'Planned, documented, and implemented Cizaro ERP for clients. Provided training, installation, and support for Cizaro ERP. Created and executed test plans and designed test cases. Documented both functional and non-functional tests, reported and followed up on bugs. Developed desktop applications in C# using object-oriented programming principles such as abstraction, inheritance, and polymorphism. Managed source code repositories with GIT and validated data accuracy with SQL queries in Postgres and SQLServer.',
          color: 'purple',
          icon: 'mdi-desktop-mac',
        },
        {
          title: 'Quality Assurance Analyst',
          company: 'Punto de Pago S.A.S',
          period: 'November 2017 - September 2018',
          description: 'Built test plans and designed test cases. Executed and documented both functional and non-functional tests, reported and followed up on bugs. Certified production steps and performed regression testing of test plans. Validated data accuracy with SQL queries in SQLServer.',
          color: 'red',
          icon: 'mdi-check-circle',
        },
      ],
      education: [
        {
          degree: 'Ingeniería de Sistemas',
          institution: 'UNAD',
          period: 'August 2022',
          description: 'Graduated with a focus on system engineering. Acquired advanced knowledge in software development and system management.',
        },
        {
          degree: 'Técnico Profesional en Desarrollo de Software',
          institution: 'Fundación Universitaria Compensar',
          period: 'May 2021',
          description: 'Specialized in software development, including programming, software engineering principles, and development practices.',
        },
      ],
      skills: [
        {
          name: 'Agile Methodologies',
          value: 85,
        },
        {
          name: 'Database Testing',
          value: 80,
        },
        {
          name: 'Programming Knowledge',
          value: 90,
        },
        {
          name: 'Software Testing Techniques',
          value: 95,
        },
        {
          name: 'Test Automation',
          value: 90,
        },
        {
          name: 'Tools Knowledge',
          value: 85,
        },
      ],
      languages: [
        {
          name: 'English',
          level: 'Fluent',
        },
        {
          name: 'Spanish',
          level: 'Native',
        },
      ],
    };
  },
};
</script>

<style scoped>
.header-section {
  background-color: #1e1e1e;
  color: #e0e0e0;
  padding: 20px 0;
}

.profile-picture {
  border: 2px solid #444;
}

.timeline-item {
  margin-bottom: 16px;
}

.timeline-card {
  background-color: #333;
  color: #e0e0e0;
  padding: 16px;
}

.v-card {
  background-color: #222;
  color: #e0e0e0;
}

@media (max-width: 600px) {
  .timeline-item {
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
  .timeline-card {
    margin-bottom: 8px;
  }
}
</style>
