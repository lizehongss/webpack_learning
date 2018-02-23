<template>
	<div>
		<h1>首页</h1>
	<router-link to="/about">go to about</router-link>
	<br>
	{{count}}
	<button @click="handleIncrement">+1</button>
	<button @click="handleDecrease">-1</button>
	</div>
</template>
<script>
	export default{
		computed:{
			count(){
				return this.$store.state.count;
			}
		},
		methods: {
			handleIncrement(){
				this.$store.commit('increment');
			},
			handleDecrease(){
				this.$store.commit('decrease');
			}
		}
	}
</script>