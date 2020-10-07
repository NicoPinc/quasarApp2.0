<template>
<div class="Cards">
        <q-card class="my-card">
      <q-img
        src="https://cdn.quasar.dev/img/parallax2.jpg"
        basic
      >
        <div class="absolute-bottom text-h6">
            {{item}}
        </div>
      </q-img>

      <q-card-section>
        {{ item }}
      </q-card-section>
    </q-card>
</div>
</template>

<script>
export default {
    name: 'card',
    props: {
        title: {
            type: String,
            required: true
        },
        description: {
            type: String,
            default: '',
        },
        to: {
            type: String,
            default: '#'
        },

    }
}
</script>
<style lang="sass">
.my-card
  width: 350px
  max-width: 100%
  
</style>