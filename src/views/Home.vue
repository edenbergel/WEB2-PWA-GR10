<template>
	<div class="home">
		<Classement msg="Welcome to Your Vue.js App"/>
		<Classement @updateMessage="title = $event" :msg="title"/>
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