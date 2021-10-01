<template>
    <v-simple-table>
        <template v-slot:default>
            <thead>
                <tr>
                    <th colspan="1" class="text-left">
                        Posição
                    </th>
                    <th colspan="2" class="text-left">
                        Clube
                    </th>
                    <th colspan="3" class="text-left">
                        Pontos
                    </th>
                </tr>
            </thead>
            <tbody>
                <tr
                    v-for="(time, index) in times"
                    :key="time.id"
                >
                    <td >{{ index + 1}}</td>
                    <td >
                        <v-avatar size="20">
                            <img :src="time.escudo" :alt="time.nome"/>
                        </v-avatar>
                        <span>{{ "   " + time.nome }}</span>
                    </td>
                    <td></td>
                    <td>{{ time.pontos }}</td>
                </tr>
            </tbody>
        </template>
    </v-simple-table>    
</template>

<script>
export default {
    name: 'ClubesTabela',
    props: {
        times: {
            type: Array,
            required: true
        }
    }
}
</script>

<style scoped>

</style>
