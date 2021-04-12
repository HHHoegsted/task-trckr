<template>
	<button 
		class="btn"
		@click="onClick()"
		:style="{background: color}"
	> 
		{{ text }} 
	</button>
</template>

<script>
export default {
	name: 'Button',
	props:{
		text:{
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
			this.$emit('btn-click');
		}
	}
}
</script>