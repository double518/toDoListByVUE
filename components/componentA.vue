<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button v-on:click="onClickMe">open mouse!</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'hello from component a'
    }
  },
  props:['msgfromfather'],
  methods: {
    onClickMe: function(){
      //console.log(this.msgfromfather)
      this.$emit('child-tell-me-sth', this.msg)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-weight: normal;
}
</style>
