<template>
	<div class="classement_container">
		<!-- <h1 v-if="isShow">{{ msg }}</h1>
		<h1 v-else>{{ msg }} !</h1>
		<h1>{{ bigMessage }}</h1>
		<h1 @click="toogleShow()">{{ isShow }}</h1>
		<h1 @click="$emit('updateMessage', 'un autre message')">{{ isShow }}</h1> -->
		<div class="classement_bloc" v-for="classement in classements" :key="classement.id">
			<div class="bloc_left">
				<h1>{{ classement.player }}</h1>
			</div>
			<div class="bloc_right">
				<div>
					<h1>{{ classement.points }}</h1> 
					<span>points</span>
				</div>
				<div>
					<h1>{{ classement.rebonds }}</h1> 
					<span>rebonds</span>
				</div>
				<div>
					<h1>{{ classement.assists }}</h1> 
					<span>assists</span>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import classements from '../data/classement.json';

export default {
	name: 'Classement',
	props: {
		msg: String,
	},
	data() {
		return {
			isShow: false,
			classements
		}
	},

	// created() {
	// 	console.log('création')
	// },
	// mounted() {
	// 	console.log('ajouté au DOM')
	// },
	
	computed: {
		bigMessage() {
			return this.msg + '!!!!'
		}
	},
	methods: {
		toogleShow() {
			this.isShow = !this.isShow
		}

	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
	@import "../scss/home.scss";
</style>