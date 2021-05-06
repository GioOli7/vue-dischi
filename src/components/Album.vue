<template>
	<div class="album">
		<img class="poster" :src="details.poster" alt="" />
		<!-- titolo -->
		<h3>{{ details.title }}</h3>
		<!-- autore -->
		<span>{{ details.author }}</span>
		<!-- anno -->
		<span>{{ details.year }}</span>
		<!-- genere -->
		<span>{{ details.genre }}</span>
	</div>
</template>

<script>
	export default {
		name: 'Album',
		props: ['details'],
	};
</script>

<style scoped lang="scss">
	.album {
		display: flex;
		flex-direction: column;
		align-items: center;
		padding: 20px;
		background-color: #2e3a46;
	}

	.poster {
		width: 150px;
		height: 150px;
	}

	span {
		display: block;
	}
</style>
