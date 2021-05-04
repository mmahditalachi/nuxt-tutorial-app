<template>
<CardDeck/>
</template>

<script>
import CardDeck from '../components/CardDeck'

  export default {
    data() {
      return {
        show: false,
        message : "mohiii",
         todos: [
      { text: 'Learn JavaScript' },
      { text: 'Learn Vue' },
      { text: 'Build something awesome' }
    ]
      }
    },
    methods: {
      showList() {
        this.show = true
      },
    },
    components :{
      CardDeck
    }
  }
</script>

<style>

</style>
