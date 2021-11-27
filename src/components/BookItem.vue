<template>
    <td>{{ bookObject.title }}</td>
    <td>{{ bookObject.author }}</td>
    <td>{{ bookObject.checkedIn }}</td>
    <td><Btn msg="Emit Me" @click="click"/></td>
</template>

<script>
import Btn from './Btn.vue'

export default {
    components: {
        Btn
    },
    props: {
        bookObject: Object
    },
    methods: {
        click(event) {
            console.log(event)
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