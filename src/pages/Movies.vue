<template>
<div>
    <input type="text" placeholder="Movie name" v-model="UsrInName">
    <button v-on:click=AddMovie()>button</button>
<ul>
    <li v-for="(item) in movielist" :key="item">
        <card />
    </li>
</ul>
</div>
</template>

<script>
import card from 'components/card.vue'

export default {
    components: { card },
    data(){
        return{
            movielist: ["Wall-e","Simpsonovi"]
        }
    },

    
}
</script>

