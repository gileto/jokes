<template>
    <li v-bind:class="{done: anec.liked}">
    <span>{{anec.joke}}</span>
    <button v-bind:class="{doneBtn: anec.liked}" v-on:click="likeStorage"> Like </button>
    </li>
    
</template>

<script>
export default {
    props: {
        anec: {
        }
    },
    methods: {
       likeStorage() {
           this.anec.liked = !this.anec.liked
           if (this.anec.liked) {
               localStorage.setItem("joke_" + this.anec.id, this.anec.liked)
           } else {
               localStorage.removeItem("joke_" + this.anec.id)
           }
           
       } 
    },
}

</script>

<style scoped> 
    li {
    display: flex;
    border: 1px solid gray;
    padding: 20px;
    margin-bottom: 10px;
    }

    span {
        margin-right: 10px;
    }

    button {
        background: transparent;
        border: 1px solid gray;
        border-radius: 10px;
        margin-left: auto;
        color: gray;
        transition: all ease 0.5s;
        cursor: pointer;
        height: 32px;
        align-self: center;
    }

    button:hover {
        transform: scale(1.2);
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
