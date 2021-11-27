<template>
    <button class="btn">{{ msg }}</button>
</template>

<script>
export default {
    name: 'Btn',
    props: {
        msg: String
    }
}
</script>

<style scoped src="../style/button.css">
</style>