<template>
  <div class="hello">
    <h3>Movies</h3>
    <ol>
      <li>Spirited Away</li>
      <li>The one with the cat</li>
      <li>Wall-e</li>
      <li>Resident evil</li>
      <li>Rohlik</li>
    </ol>
    {{ k}}
    <ol>
      <li v-for="(item,index) in movielist" :key="item">
        {{ item }}  <button v-on:click=DeleteThis(index)>DELETE this</button>
      </li>
    </ol>
      <input id="input" type="text" placeholder="add item" v-model="usrinput" >
      <button v-on:click=AddMovie()>button</button> <br><br><br><br><br>
      {{reversed}} <br><br> 
      <button v-on:click=DeleteLast()>DELETE last one</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return{
      usrinput: "",
      k:"Hello, how are you.",
      movielist: ["walle","test"],
    }
  },
    methods:{  
      AddMovie(){
      this.movielist.push(this.usrinput)
      },
      DeleteThis(index){
        this.movielist.splice(index, 1);
      },
    },
    computed:{
    reversed(){
    return this.usrinput.split('').reverse().join('')
    },
    },

}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ol {
  text-align: center;
  margin-block: 10px;
}
</style>
