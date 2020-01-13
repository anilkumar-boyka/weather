<template>

<div>
	<!-- City:<select>
      <option>London</option>
      <option>France</option>
      <option>Moscow</option>

    </select> -->
	

<button type="button">Check Weather</button>
 <input v-model="input" placeholder="select city">
   {{input}} 
      
 
</div>
    

    </template>
    <script>


   export default {
  name: 'Button',
  data () {
    return {
      input:null
    }
  }
}
</script> 