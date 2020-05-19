<template>
	<div class="home">
		<h3>Le Classement de la Semaine</h3>
		<Classement />
	<!-- 	<Classement @updateMessage="title = $event" :msg="title"/> -->
	</div>
</template>

<script>
import Classement from '@/components/Classement.vue'

export default {
	name: 'Home',
	data() {
		return {
			title: 'ceci'
		}
	},
	components: {
		Classement,
	}
}
</script>

<style lang="scss" scoped>
	@import "../scss/home.scss";
</style>