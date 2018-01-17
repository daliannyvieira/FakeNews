<template>
	<nav class='menu'>
		<img class='menu-icone' src='../assets/menu hamburguer.svg' alt='menu'>
		<h1 class='menu-titulo'>FAKENEWS</h1>
		<img class='menu-icone' src='../assets/Lupa-busca.svg' alt='busca'>
	</nav>
</template>

<style> 
	.menu {
		display: flex;
		justify-content: space-between;
		padding: 0.5rem;
		margin: 0;
		background: black;
	}
	.menu-titulo {
		margin: 0;
		color: #fff;
	}
	.menu-icone {
		max-width: 2rem;
	}
</style>