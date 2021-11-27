<template>
    <label>{{ label }}</label>
    <input
       type="text"
       :value="modelValue"
       @input="$emit('update:modelValue', $event.target.value)"
       @change="$emit('textChange', $event.target.value)"
    >
</template>

<script>
export default {
    props: {
        label: String,
        modelValue: String
    },
    emits: ['update:modelValue', 'textChange']
};
</script>
