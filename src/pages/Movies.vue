<template>
<div>
    <div class="inputMovies">
    Wanna add Movie ? <br>
    <input type="text" placeholder="Enter movie name" v-model="UsrInName">
    <input type="text" placeholder="Movie Description" v-model="UsrInDescr" >
    <button class="movieButt" v-on:click=AddMovie()>button</button>
    </div>
    <div class="moviecard">
    <card v-for="item in movielist" :key="item.movielist" v-bind:movielist="item">
    </card>
    </div>
</div>
</template>

<script>
import card from 'components/card.vue'

export default {
    name: 'Movies',
    components: { card },
    data(){
        return{
            UsrInDescr: "",
            UsrInName: "",
            movielist: []
        }
    },
    methods: {
        AddMovie() {
            console.log(this.UsrInName),
            this.movielist.push({movieName: this.UsrInName, movieDescr: this.UsrInDescr})

        }
    }
    
}
</script>

<style lang="sass">
.moviecard
    display: flex
    justify-content: center
    flex-direction: row
    flex-wrap: wrap
    align-content: flex-start
    align-self: flex-auto
.inputMovies
    text-align: center
    padding: 10px
.movieButt
    margin-left: 15px
</style>