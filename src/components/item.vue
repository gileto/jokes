<template>
    <li v-bind:class="{done: anec.liked}">
    {{anec.text}}
    <button v-bind:class="{doneBtn: anec.liked}"> Like </button>
    </li>
</template>

<script>
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

    .done {
        background: Honeydew;
        font-weight: bold;
        border-color: DarkGray;
    }

    .doneBtn {
        color: Black;
        background: LavenderBlush;
        border-color: Orchid;

    }

</style>
