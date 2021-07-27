<template>
    <li>
    {{ anec.text}}
    </li>
</template>

<<script>
export default {
    props: {
        anec: {
        }
    }
}
</script>

<style scoped> 
    li {
    border: 1px solid gray;
    padding: 10px;
    margin-bottom: 10px;
    }
</style>
