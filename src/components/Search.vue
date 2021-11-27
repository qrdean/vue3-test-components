<template>
    <InputField 
        label="Search By Title"
        @textChange="$emit('searchEvent', $event)"
    />
</template>

<script>
import InputField from './InputField.vue'

export default {
    components: {
        InputField
    },
    emits: ['searchEvent'],
    data() {
        return {
            searchData: ''
        }
    }
}
</script>