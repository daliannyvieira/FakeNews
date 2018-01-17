<template>
	<main class="pagina">
		<Menu />
		<Postagens />
    	<Comentarios />
	</main>
</template>

<script>
	import Menu from './Menu'
	import Postagens from './Postagens'
	import Comentarios from './Comentarios'

	export default {
		components: {Postagens, Comentarios, Menu}
	}
</script>

<style scoped>
	@media (min-width: 650px) {
		.pagina {
			max-width: 70%;
		}
	}
</style>