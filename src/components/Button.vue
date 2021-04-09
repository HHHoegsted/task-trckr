<template>
	<button 
		class="btn"
		@click="onClick()"
		:style="{background: color}"
	> 
		{{ title }} 
	</button>
</template>

<script>
export default {
	name: 'Button',
	props:{
		title:{
			type: String,
			required:true,
		},
		color:{
			type: String,
			default: '#6ea5ff',
		}
	},
	methods:{
		onClick(){
			this.$emit('toggle-add-task')
		}
	}
}
</script>