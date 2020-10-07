<template>
<div>
    <input type="text" placeholder="Movie name" v-model="UsrInName">
    <button v-on:click=AddMovie()>button</button>
    <div class="moviecard">
    <card v-for="(item) in movielist" :key="item">
    </card>
    </div>
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

<style lang="sass">
.moviecard
    display: flex
    justify-content: center
    flex-direction: row
    align-content: flex-start
    align-self: flex-auto

</style>