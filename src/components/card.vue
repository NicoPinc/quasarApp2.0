<template>
<div class="Cards">
        <q-card class="my-card">
      <q-img
        src="https://cdn.quasar.dev/img/parallax2.jpg"
        basic
      >
        <div class="absolute-bottom text-h6">
            {{movielist.movieName}}
        </div>
      </q-img>

      <q-card-section>
        {{ movielist.movieDescr }}
      </q-card-section>
    </q-card>
</div>
</template>

<script>
export default {
    name: 'card',
    props: {
      movielist: {
        movieName: {
          type: String,
          required: true
        },
        movieDescr: {
          type: String,
          default: ''
        }
      }
    }
}
</script>
<style lang="sass">
.my-card
  width: 350px
  max-width: 100%
  
</style>