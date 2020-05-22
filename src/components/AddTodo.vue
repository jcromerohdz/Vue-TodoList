<template>
	<div>
		<form @submit.prevent @submit="addTodo">
			<input type="text" v-model="title" name="title" placeholder="Add Todo...">
			<input type="submit" value="Submit" class="btn">
		</form>
	</div>
</template>

<script>
//import { v4 as uuidv4 } from 'uuid';

export default {
	name: "AddTodo",
	data () {
		return {
			title: ''
		}
	},
	methods:{
		addTodo() {
			const newTodo = {
				title: this.title,
				copleted: false
			}
			// Send up to parent
			this.$emit('add-todo', newTodo)
			this.title = '';
		}
	}
}
</script>

<style scoped>
	form {
		display: flex;
	}

	input[type="text"] {
		flex: 10px;
		padding: 5px;
	}

	input[type="text"] {
		flex: 2
	}
</style>