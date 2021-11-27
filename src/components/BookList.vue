<template>
    <table>
    <tr>
        <th>Title</th>
        <th>Author</th>
        <th>Checked In</th>
        <th/>
    </tr>
    <tr v-for="bookObject in bookObjects" v-bind:key="bookObject.id">
        <td>{{ bookObject.title }}</td>
        <td>{{ bookObject.author }}</td>
        <td>{{ bookObject.checkedIn }}</td>
        <td><Btn msg="Checkout" @click="click(bookObject)"/></td>
    </tr>
</table>
</template>


<script>
import Btn from './Btn.vue'

export default {
    components: {
        Btn
    },
    props: {
        bookObjects: [Object],
    },
    methods: {
        click(bookObject) {
            console.log('checkout: ', bookObject.id)
        }
    }
}
</script>

<style scoped>
table {
    border-collapse: collapse;
    width: 100%;
}

td, th {
    border: 1px solid #dddddd;
    text-align: left;
    padding: 8px;
}
</style>