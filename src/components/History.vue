<template>
  <v-container fluid id="history" class="white">
    <v-layout text-center wrap mt-5 mb-5>
      <v-row justify="center">
        <v-col class="col-12">
          <h1 class="display-3 font-weight-bold mb-3 black--text">History</h1>
        </v-col>
        <v-col class="col-8">
          <v-timeline>
            <v-timeline-item
              v-for="(history, key) in histories"
              :key="key"
              large
            >
              <template v-slot:icon>
                <v-avatar color="white">
                  <!-- <img src="@/assets/img/companies/rock.png"> -->
                  <img :src="history.company_image">
                </v-avatar>
              </template>
              <template v-slot:opposite>
                <span>{{ history.range }}</span>
              </template>
              <v-card class="elevation-2">
                <v-card-title class="headline">{{ history.company_name }}</v-card-title>
                <v-card-text>{{ history.description }}</v-card-text>
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
        range : 'Atualmente',
        company_name: 'Rock Content',
        company_image: 'https://media.licdn.com/dms/image/C560BAQEH4QpFN2LMWA/company-logo_400_400/0?e=1579737600&v=beta&t=WZNWLZeLtl_XInBir0QCL3KgnrZ7zV59_D6iGC-9lLM',
        description: 'testesetste'
      },
      {
        range : '2019',
        company_name: 'TCS',
        company_image: 'https://media.licdn.com/dms/image/C4E0BAQGgJEEcnjca4w/company-logo_400_400/0?e=1579737600&v=beta&t=N-XL5Z62otNPagJ1HxpYHYdMU3nAjMLSMOkKGga9mV0',
        description: 'testesetste'
      },
      {
        range : '2018-2019',
        company_name: 'Diários Associados',
        company_image: 'https://media.licdn.com/dms/image/C4E0BAQElSebak7qh8A/company-logo_400_400/0?e=1579737600&v=beta&t=VLQI0Ez2_a708NopJ94-E_589jb6q3YlKqcZDH9803Q',
        description: 'testesetste'
      },
      {
        range : '2017-2018',
        company_name: 'Grupo Andrade Martins',
        company_image: 'https://media.licdn.com/dms/image/C4E0BAQE620YARHK-Tg/company-logo_400_400/0?e=1579737600&v=beta&t=VpgTX9Z9uD4FQEaYIYp9kx1LJJGTJfLYCHNgQFaKKsg',
        description: 'testesetste'
      },
      {
        range : '2016-2017',
        company_name: '360e1 Entretenimento',
        company_image: 'https://media.licdn.com/dms/image/C510BAQGAe09pk2iVnA/company-logo_400_400/0?e=1579737600&v=beta&t=a8MPdl5jC41bT5HvAQ-2JxdhqnjS4bnU95_YIbbbGdg',
        description: 'testesetste'
      },
    ]
  }),
};
</script>
