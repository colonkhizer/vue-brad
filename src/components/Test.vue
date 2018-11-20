<template>
	<div>
		<input type="text" v-model="msg">
		{{ msg }}
		<div>
			{{users.firstName}}
			{{ users.lastName}}
		</div>				
		<div v-for="item in products">
			{{ item.title }}
		</div>
		<button v-on:click="greet">Check Message</button><br />
		<input type="text" v-on:keyup="pressKey" v-on:keyup.enter="enterHit"/>
		<hr/>
		<label>First Name :</label><input type="text" v-model="users.firstName"/>
		<br/>
		<label>Last Name :</label><input type="text" v-model="users.lastName"/>
		<br/>{{ fullName }}
	</div>
</template>

<script>
	export default {
		name: 'Test',
		props: {
	    msg: String
	  	},		
		data (){
			return{
				users: {
				      firstName: 'Khizer',
				      lastName: 'Syed'
						},
				products: [
					{title: 'New'},
					{title: 'Old'},
					{title: 'Reserved'}
				]
			}
		},
		methods: {
	  		greet: function () {
	  			alert('Greet Clicked')
	  		},
	  		pressKey : function(e) {
	  			console.log(e.target.value)
	  		},
	  		enterHit: function() {
	  			console.log('You have Entered Hit')
	  		}
	  	},
	  	computed :{
	  		fullName: function () {
	  			return this.users.firstName+ ' ' +this.users.lastName
	  		}
	  	}
	}
</script>

<style>
	
</style>