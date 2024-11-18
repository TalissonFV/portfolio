<template>
    <v-container class="fill-height">
      <v-responsive
        class="align-centerfill-height mx-auto"
        max-width="1200"
      >
      <div class="py-4" />

      <div class="text-center" style="font-family: 'Fragment Mono', monospace;">
        <h1 class="text-h2 font-weight-bold" style="font: inherit;vertical-align: baseline;">Talisson Ferreira Vilela</h1>
        Desenvolvedor Web <span class="type">
            <span>
            <span>Fullstack</span>
            <span>Backend</span>
            <span>Frontend</span>
          </span>
        </span>
      </div>
      <div class="py-4" />
      <v-row>
          <v-col cols="3">
            <v-img
            style="border-radius: 100%;"
              :width="200"
              aspect-ratio="4/3"
              class="rounded"
              cover
              src="https://media.discordapp.net/attachments/1250904316311633933/1307875261525659719/tinywow_IMG_20240829_154959_69453046.png?ex=673be541&is=673a93c1&hm=a2f573760ca06391012478f34558defeaf6298df02d07d15708f21125575700f&=&format=webp&quality=lossless"
            ></v-img>
            <a
                  v-for="item in socials"
                  :key="item.title"
                  :href="item.href"
                  :title="item.title"
                  class="d-inline mx-2 social-link"
                  rel="noopener noreferrer"
                  target="_blank"
                >
                  <v-icon
                    :icon="item.icon"
                    :size="item.icon === '$vuetify' ? 24 : 16"
                  />
                </a>
          </v-col>

          <v-col cols="9">
            <v-card
              class="py-4 text-center"
              color="surface-variant"
              rounded="lg"
              variant="text"
              title="Sobre Mim"
            >
              <template #text>
                <div>
                    Nascí em Jataí-GO e comecei a programar aos 13 anos quando entrei no Instituto Federal de Goiás no curso Tecnico em Informática integrado ao Ensino Médio.
                    Me formei em Sistemas de Informação em 2019. Fiz estágio em uma Startup onde comecei aprender Vue.js e Node.js. Trabalhei 4 anos em uma empresa da area de planos de saúde como Desenvolvedor Web Fullstack
                    onde pude fazer parte da criação de um Modulo de ERP interno da companhia e desenvolver APIs para integração de dados de parceiros e outros projetos internos.
                </div>
              </template>
  
              <v-overlay
                opacity=".12"
                scrim="primary"
                contained
                model-value
                persistent
              />
            </v-card>
            
          </v-col>

      </v-row>
        <div class="py-4" />
  
        <v-row>
          
          <v-col cols="12">
            <v-card
              class="py-4"
              color="surface-variant"
              prepend-icon="mdi-star-circle-outline"
              rel="noopener noreferrer"
              rounded="lg"
              title="Habilidades"
              variant="text"
              >
              
              <v-overlay
                opacity=".06"
                scrim="primary"
                contained
                model-value
                persistent
              />
              <v-row>
                <v-col cols="3" v-for="(habilidade, index) in habilidades">
                  <v-card :prepend-icon="habilidade.icon" class="text-center px-2 mx-1" :title="habilidade.nome"></v-card>
                </v-col>
              </v-row>
            </v-card>
          </v-col>
        
          <v-col cols="12">
              <v-card
              class="py-4"
              color="surface-variant"
              prepend-icon="mdi-text-box-outline"
              rel="noopener noreferrer"
              rounded="lg"
              target="_blank"
              title="Experiências"
              variant="text"
              >
                  <v-overlay
                      opacity=".06"
                      scrim="primary"
                      contained
                      model-value
                      persistent
                  />
                  <v-list density="compact">

                      <v-list-item
                          v-for="(item, i) in experiencias"
                          :key="i"
                          :value="item"
                          color="primary"
                      >

                          <v-list-item-title class="font-bold">{{ `${item.nome} - ${item.cargo} `}}</v-list-item-title>
                          <v-list-item-text>{{ `${item.dataInicio} - ${item.dataFim}` }}</v-list-item-text>
                          <v-divider :thickness="4" color="info"></v-divider>
                            <v-list density="compact">

                              <v-list-item
                                  v-for="(atividade, i) in item.atividades"
                                  :key="i"
                                  :value="item"
                                  color="primary"
                              >
                                  <v-list-item-text>{{ atividade.descricao }}</v-list-item-text>
                                  
                              </v-list-item>
                            </v-list>
                      </v-list-item>
                  </v-list>
              </v-card>
          </v-col>
  
        </v-row>
      </v-responsive>
    </v-container>
  </template>
  
<script setup lang="ts">
    // TypeScript enabled
    const experiencias = [
        {
            nome: "Qualicorp",
            cargo: "Analista de Sistemas II",
            atividades: [
              {
                descricao: "- Realizei manutenção do modulo desenvolvido para ERP interno."
              },
              {
                descricao: "- Manutenção de banco de dados em grafos utilizando Neo4j."
              },
              {
                descricao: "- Realizei integrações com sistemas de mercado utilizado por parceiros."
              },
              {
                descricao: "- Criei documentação das APIs desenvolvidas."
              },
              {
                descricao: "- Realizei a configurações de Dev Ops utilizando Azure."
              },
              {
                descricao: "- Experiência utilizando sistemas open source como Gravitee, PM2, RabbitMQ."
              },
            ],
            dataInicio: "Fev de 2021",
            dataFim: "Mai de 2024"
        },
        {
            nome: "Talent Group @Qualicorp",
            cargo: "Desenvolvedor web fullstack trainee",
            atividades: [
              {
                descricao: "- Fiz parte do desenvolvimento de um novo modulo web para o ERP interno com Vue.js e Node.js."
              },
              {
                descricao: "- Criei e fiz manutenção em banco de dados de grafos com Neo4j."
              },
              {
                descricao: "- Criei API REST para integração de dados com parceiros e outros projetos internos."
              },
              {
                descricao: "- Desenvolvi integrações novas do modulo do ERP com sistemas de parceiros e de outros projetos internos."
              },
              {
                descricao: "- Participei de reuniões diárias seguindo metodologias ágeis para o desenvolvimento."
              },
            ],
            dataInicio: "Abr de 2020",
            dataFim: "Fev de 2021"
        },
        {
            nome: "Manycontent",
            cargo: "Estágio em Desenvolvimento Web",
            atividades: [
              {
                descricao: "- Desenvolvimento de novas funcionalidades no front-end usando Vue.js e no back-end usando Node.js através de cloud functions do Firebase;"
              },
              {
                descricao: "- Manutenção e desenvolvimento do banco de dados utilizando Firestore;"
              },
              {
                descricao: "- Integração da plataforma web com API's de Redes Sociais;"
              },
              {
                descricao: "- Responsável pelo suporte de 2º nível;"
              },
              {
                descricao: "- Tradução e internacionalização da plataforma web utilizando i18n;"
              },
            ],
            dataInicio: "Out de 2018",
            dataFim: "Dez de 2019"
        }
    ]

    const habilidades = [
        {
            nome: "JavaScript",
            nivel: "5",
            icon: "mdi-language-javascript"
        },
        {
            nome: "TypeScript",
            nivel: "5",
            icon: "mdi-language-typescript"
        },
        {
            nome: "NodeJS",
            nivel: "5",
            icon: "mdi-nodejs"
        },
        {
            nome: "VueJS",
            nivel: "5",
            icon: "mdi-vuejs"
        },
        {
            nome: "Neo4j",
            nivel: "5",
            icon: "mdi-graph"
        },
        {
            nome: "Git",
            nivel: "5",
            icon: "mdi-git"
        },
        {
            nome: "API",
            nivel: "5",
            icon: "mdi-api"
        },
        {
            nome: "SQL/NoSQL",
            nivel: "5",
            icon: "mdi-database"
        },
        
        
    ]

    const socials = [
    {
      title: 'Twitter',
      icon: ['M2.04875 3.00002L9.77052 13.3248L1.99998 21.7192H3.74882L10.5519 14.3697L16.0486 21.7192H22L13.8437 10.8137L21.0765 3.00002H19.3277L13.0624 9.76874L8.0001 3.00002H2.04875ZM4.62054 4.28821H7.35461L19.4278 20.4308H16.6937L4.62054 4.28821Z'],
      href: 'https://x.com/tallvile',
    },
    {
      title: 'GitHub',
      icon: `mdi-github`,
      href: 'https://github.com/talissonfv',
    },
    {
      title: 'Discord',
      icon: ['M22,24L16.75,19L17.38,21H4.5A2.5,2.5 0 0,1 2,18.5V3.5A2.5,2.5 0 0,1 4.5,1H19.5A2.5,2.5 0 0,1 22,3.5V24M12,6.8C9.32,6.8 7.44,7.95 7.44,7.95C8.47,7.03 10.27,6.5 10.27,6.5L10.1,6.33C8.41,6.36 6.88,7.53 6.88,7.53C5.16,11.12 5.27,14.22 5.27,14.22C6.67,16.03 8.75,15.9 8.75,15.9L9.46,15C8.21,14.73 7.42,13.62 7.42,13.62C7.42,13.62 9.3,14.9 12,14.9C14.7,14.9 16.58,13.62 16.58,13.62C16.58,13.62 15.79,14.73 14.54,15L15.25,15.9C15.25,15.9 17.33,16.03 18.73,14.22C18.73,14.22 18.84,11.12 17.12,7.53C17.12,7.53 15.59,6.36 13.9,6.33L13.73,6.5C13.73,6.5 15.53,7.03 16.56,7.95C16.56,7.95 14.68,6.8 12,6.8M9.93,10.59C10.58,10.59 11.11,11.16 11.1,11.86C11.1,12.55 10.58,13.13 9.93,13.13C9.29,13.13 8.77,12.55 8.77,11.86C8.77,11.16 9.28,10.59 9.93,10.59M14.1,10.59C14.75,10.59 15.27,11.16 15.27,11.86C15.27,12.55 14.75,13.13 14.1,13.13C13.46,13.13 12.94,12.55 12.94,11.86C12.94,11.16 13.45,10.59 14.1,10.59Z'],
      href: 'https://discord.gg/Vg3fZa6a',
    },
  ]
</script>

<style>


.type {
  display:inline-block;
}
.type > span {
  display:grid;
  overflow: hidden;
  height:1.2em;
}
.type span span {
  width:0%;
  max-width:max-content;
  overflow: hidden;
  height:inherit;
  word-break:break-all;
  animation:
    c 0.5s infinite steps(1),  
    t 2s linear infinite alternate,
    m 12s steps(3) infinite;
}
.type span span:before {
  content:" ";
  display:inline-block;
}
@keyframes t{
  90%,100% {width:100%}
}
@keyframes c{
  0%,100%{box-shadow:5px 0 0 #0000}
  50%    {box-shadow:5px 0 0 red  }
}
@keyframes m{
  100% {transform:translateY(-300%)}
}



</style>
  