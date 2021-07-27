<template>
<div>
<ul>
<item/>
</ul>
</div>
</template>

<script>
import item from '@/components/item'
export default {
    components: {
        item
    }
}
</script>

<style scoped> 
ul {
list-style-type: none;
border: 1px solid gray;
margin: 0 auto;
max-width: 1000px;
padding: 20px;
}
</style>