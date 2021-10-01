<template>
    <v-container>
        <h2 class="Titulo">
            Classificação dos Clubes
        </h2>
        <ClubesTabela :times="TimesOrdenados"/>
    </v-container>
</template>

<script>
import ClubesTabela from '../components/ClubesTabela.vue'

export default {
    name: 'ClubesLista',
    components: {
        ClubesTabela
    },
    data() {
        return {
            TimesLista: []
        }
    },
    created() {
        fetch('https://hackthon-decola.firebaseio.com/clubes-lista.json')
        .then(response => response.json())
        .then(json => {
            this.TimesLista = json
        })
    },
    computed: {
        TimesOrdenados (){
            const listaComputada = this.TimesLista.slice(0).sort(
                (a, b) => a.pontos > b.pontos ? -1 : 1
            );
            return listaComputada;
        }
    }
}
</script>

<style scoped>

</style>
