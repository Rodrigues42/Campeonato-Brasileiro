<template>
    <v-simple-table>
        <template v-slot:default>
            <thead>
                <tr>
                    <th class="text-left">
                        Clube
                    </th>
                    <th class="text-left">
                        Pontos
                    </th>
                </tr>
            </thead>
            <tbody>
                <tr
                    v-for="item in desserts"
                    :key="item.name"
                >
                    <td>{{ item.name }}</td>
                    <td>{{ item.calories }}</td>
                </tr>
            </tbody>
        </template>
    </v-simple-table>    
</template>

<script>
export default {
    data() {
        
    },
}
</script>

<style scoped>

</style>
