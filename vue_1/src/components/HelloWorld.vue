<template>
 	<table>
	<tr v-for="user in users">
		<th></th>
	</tr>
 	</table>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
  	return({
  		users: {}
  		});
  },
  created: function(){
  	this.users = fetch('https://gorest.co.in/public-api/users?_format=json&access-token=zbduG6SiEK7TekrUcCzWYrZPEKbWt49RcW-f')
  	.then(response => response.json())
  	.then(json => console.log(JSON.stringify(json)))
  },
  props: {
	msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
