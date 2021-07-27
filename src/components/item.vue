<template>
    <li>
    {{anec.text}}
    <button>Like</button>
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
    display: flex;
    border: 1px solid gray;
    padding: 20px;
    margin-bottom: 10px;
    }


    button {
        padding: 10px;
        background: transparent;
        border: 1px solid gray;
        border-radius: 10px;
        margin-left: auto;
        color: gray;
    }
</style>
