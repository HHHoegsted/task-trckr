<template>
	<header>
		<h1>{{ title }}</h1>
		<Button 
			@btn-click="$emit('toggle-add-task')"
			:text="showAddTask ? 'Close': 'Add Task'"
			:color="showAddTask ? '#ff584d' : '#54e858'"
		/>
		
	</header>
</template>

<script>
import Button from './Button';

export default {
	name: 'Header',
	props:{
		title: String,
		showAddTask: Boolean,
	},
	components:{
		Button
	},
	emits:[
		'toggle-add-task',
	],
	computed:{
		homePage(){
			return this.$route.path === '/';
		}
	}
}
</script>

<style scoped>
header{
	display: flex;
	justify-content: space-between;
	align-items: center;
	margin-bottom: 20px;
}
</style>