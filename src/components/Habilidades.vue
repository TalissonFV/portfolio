<template>
    <v-col cols="12">
        <v-card
        class="py-4"
        color="surface-variant"
        prepend-icon="mdi-star-circle-outline"
        rel="noopener noreferrer"
        rounded="lg"
        target="_blank"
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
            <v-col cols="3" v-for="(habilidade) in habilidades">
                <v-card :prepend-icon="habilidade.icon" class="text-center px-4 mx-1" :title="habilidade.nome"></v-card>
            </v-col>
        </v-row>
        </v-card>
    </v-col>
</template>

<script lang="ts">
const habilidades = [
        {
            nome: "JavaScript",
            nivel: "5",
            icon: "mdi-language-javascript"
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
        
    ]
</script>