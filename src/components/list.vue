<template>
<div>
    <ul>
        <item 
            v-for="anec of anecdotes"
            v-bind:anec="anec"
        />
    </ul>
</div>
</template>

<script>
import item from '@/components/item'
export default {
    props: ['anecdotes'],
    components: {
        item
    }
}
</script>

<style scoped> 
ul {
list-style-type: none;
border: 1px solid gray;
margin: 0 auto 50px auto;
max-width: 1000px;
padding: 20px;
}
</style>