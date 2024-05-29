<template>
<div>
  <h1> FirstName = {{firstName}}</h1>
  <input v-model="firstName" type="text" placeholder="Nhap firstName">
  <br>
  <p> {{message}}</p>
  <p> {{reverseMessage}}</p>
<!--  <p> {{reverseMessage()}}</p>-->
  <br>
  <button v-on:click="a++">A = A + 1 </button>
  <button v-on:click="b++">B = B + 1 </button>
  <p>Number + A = {{addA}}</p>
  <p>Number + B = {{addB}}</p>
</div>
</template>

<script>
export default {
  name: "computedProps",
  data () {
    return {
      message: 'Hello world',
      a: 0,
      b: 0,
      number: 20,
      firstName:''
    }
  },
  methods: {
    // reverseMessage: function () {
    //   return this.message.split('').reverse().join('')
    // },
    // addA(){
    //   console.log('addA run');
    //   return this.a + this.number
    // },
    // addB(){
    //   console.log('addB run');
    //   return this.b + this.number
    // },
  },
  computed: {
    reverseMessage: function () {
      return this.message.split('').reverse().join('')
    },
    addA(){
      console.log('addA run');
      return this.a + this.number
    },
    addB(){
      console.log('addB run');
      return this.b + this.number
    },
  },
}

</script>

<style scoped>

</style>