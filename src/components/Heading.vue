<template>
	<div style="font-size:30px ;color:red">
		Weather report <br>
		{{message.currently.temperature +"  "+message.timezone}}


	</div>
</template>

 
<script>

  import axios from "axios"
	export default {
		name: "Heading",
		data(){
			return {
				message: "null"
			}
		},
		methods: {
			fetch_data(){
				axios
				.get('https://cors-anywhere.herokuapp.com/https://api.darksky.net/forecast/753119c50b95369b12bd2bf504416c09/42.3601,-71.0589', {
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