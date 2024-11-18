<template>
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
      
</template>

<script lang="ts">
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
</script>