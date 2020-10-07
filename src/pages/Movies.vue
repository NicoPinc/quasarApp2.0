<template>
<div>
    <div class="inputMovies">
    Wanna add Movie ? <br>
    <input type="text" placeholder="Enter movie name" v-model="UsrInName">
    <button class="movieButt" v-on:click=AddMovie()>button</button>
    </div>
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
    methods: {
        AddMovie() {
            this.movielist.push(this.UsrInName)
        }
    }
    
}
</script>

<style lang="sass">
.moviecard
    display: flex
    justify-content: center
    flex-direction: row
    align-content: flex-start
    align-self: flex-auto
.inputMovies
    text-align: center
    padding: 10px
.movieButt
    margin-left: 15px
</style>