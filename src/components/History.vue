<template>
  <v-container fluid id="history" class="white">
    <v-layout text-center wrap mt-5 mb-5>
      <v-row justify="center">
        <v-col class="col-12">
          <h1 class="display-3 font-weight-bold mb-3 black--text">History</h1>
        </v-col>
        <v-col class="col-12 col-sm-8">
          <v-timeline class="d-none d-lg-block">
            <v-timeline-item
              v-for="(history, key) in histories"
              :key="key"
              large
            >
              <template v-slot:icon>
                <v-avatar color="white">
                  <img :src="history.company_image">
                </v-avatar>
              </template>
              <template v-slot:opposite>
                <span>{{ history.range }}</span>
              </template>
              <v-card class="raised-4">
                <v-card-title class="title">{{ history.company_name }}</v-card-title>
                <v-card-text class="text-justify body-1">{{ history.description }}</v-card-text>
              </v-card>
            </v-timeline-item>
          </v-timeline>
          <v-timeline :reverse="true" dense class="d-block d-lg-none">
            <v-timeline-item
              v-for="(history, key) in histories"
              :key="key"
              large
            >
              <template v-slot:icon>
                <v-avatar color="white">
                  <img :src="history.company_image">
                </v-avatar>
              </template>
              <template v-slot:opposite>
                <span>{{ history.range }}</span>
              </template>
              <v-card class="raised-4">
                <v-card-title class="title">{{ history.company_name }}</v-card-title>
                <v-card-text class="text-justify body-1">{{ history.description }}</v-card-text>
              </v-card>
            </v-timeline-item>
          </v-timeline>
        </v-col>
      </v-row>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    histories: [
      {
        range : 'Aug 2019 - Currently',
        company_name: 'Rock Content',
        company_image: 'https://media.licdn.com/dms/image/C560BAQEH4QpFN2LMWA/company-logo_400_400/0?e=1579737600&v=beta&t=WZNWLZeLtl_XInBir0QCL3KgnrZ7zV59_D6iGC-9lLM',
        description: "Acting as fullstack in the development of new products in microservices format, using technologies such as Node, Vue, Express, MongoDb, Docker. I am part of a team that deals directly with the company's strategic decisions, generating great values ​​through technology."
      },
      {
        range : 'Jun 2019 - Aug 2019',
        company_name: 'TCS',
        company_image: 'https://media.licdn.com/dms/image/C4E0BAQGgJEEcnjca4w/company-logo_400_400/0?e=1579737600&v=beta&t=N-XL5Z62otNPagJ1HxpYHYdMU3nAjMLSMOkKGga9mV0',
        description: 'I worked as a developer in an urban mobility project. I used the technologies Node, Vue, Express, MongoDB, Docker.'
      },
      {
        range : 'Feb 2018 - Jun 2019',
        company_name: 'Diários Associados',
        company_image: 'https://media.licdn.com/dms/image/C4E0BAQElSebak7qh8A/company-logo_400_400/0?e=1579737600&v=beta&t=VLQI0Ez2_a708NopJ94-E_589jb6q3YlKqcZDH9803Q',
        description: "Member of the development team of Diário Associados, developing several innovations and improvements for the group's products such as Vrum, Lugar Certo, Portal Estado de Minas, UAI, SuperSports. I use technologies like Scrum, GIT, TDD, Python, Django, Flask and database (Postgres, Oracle, REDIS)."
      },
      {
        range : 'Apr 2017 - Feb 2018',
        company_name: 'Grupo Andrade Martins',
        company_image: 'https://media.licdn.com/dms/image/C4E0BAQE620YARHK-Tg/company-logo_400_400/0?e=1579737600&v=beta&t=VpgTX9Z9uD4FQEaYIYp9kx1LJJGTJfLYCHNgQFaKKsg',
        description: "I worked as a developer on the company's own product (CRM). Acting as backend using Python, Django, Mysql and also as frontend (HTML, CSS, JavaScript, Jquery) and using SCRUM methodology."
      },
      {
        range : 'Feb 2016 - Apr 2017',
        company_name: '360e1 Entretenimento',
        company_image: 'https://media.licdn.com/dms/image/C510BAQGAe09pk2iVnA/company-logo_400_400/0?e=1579737600&v=beta&t=a8MPdl5jC41bT5HvAQ-2JxdhqnjS4bnU95_YIbbbGdg',
        description: 'Java Desktop Application Development Using JavaFx. Database creation and administration using MySQL. Requirements gathering and software design.'
      },
    ]
  }),
};
</script>
