<template>
        <input type="text" placeholder="Поиск по слову: ввести слово и нажать Enter" v-on:input="onChange"></input>
</template>

<script>
export default {
    methods: {
        onChange(e) {
            this.$emit('search', e.target.value)
        }
    },
}
</script>

<style scoped>
    form {
        display: flex;
        justify-content: center;
        margin-bottom: 30px;
        border-collapse: collapse;
    }

    input {
        width: 50%;
        border: 1px solid gray;
        padding: 10px;
        margin-bottom: 20px;
    }
</style>