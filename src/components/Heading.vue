<template>
	<div style="font-size:30px ;color:red">
		<p>{{answer}}</p>
		<h2>Weather report for {{msg}}</h2><br>
    <!-- <p>you typed {{msg}}</p> -->
    {{msg}}
    
       {{message.request.query}} 
         {{message.current.temperature}}

		
         </div>        
        
</template>

 
<script>

   // import Button from './Button'
	import axios from "axios"
	export default {
		name: "Heading",
		 // components:{Button},
		data(){                       
			return {
				message1: this.msg,
				message:'',
				answer:'type city name'

			    }
			
		},
		props:['msg'],

		watch:{
      
        	msg: function (newVal, oldVal) {
        		this.answer = 'type here....'
                
        	    this.fetch_data();
        	    this.debouncedGetAnswer();

      
      		}
  		},

  		  created: function () {
  		  	this.debouncedGetAnswer = _.debounce(this.getAnswer, 500)
  		  },
   
        methods:{
            getAnswer: function () {
                 this.answer = 'Thinking...'  	
               },

        


			fetch_data(){
				console.log(this.message1);
				axios
				.get('http://api.weatherstack.com/current?access_key=f40b5d81272aa2a4f415b472e6374192&query='+this.msg, {
				})
				.then(res => {
					console.log(res)
					this.message = res.data;
				})
			}
		},
		mounted(){
			this.fetch_data()
		}
    }
	
</script>