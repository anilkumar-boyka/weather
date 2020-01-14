<template>

<div>
	
	  <h2>Type city name to check weather</h2>
 <input v-model="input"  placeholder="select city">

 <!-- <p>{{input}}</p> -->
 
 <Hello :msg="input"></Hello>
 <!-- <p>{{message}}</p> -->
     
        
  </div>
    

    </template>
    <script>
    import Heading from './Heading'


   export default {
  name: 'Button',
    components :{
      'Hello':Heading

    },
  data () {
    return {
      input:null,
      message:'hi,m anil'
       
    }
  }
}
</script> 