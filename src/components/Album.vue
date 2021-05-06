<template>
	<div class="album">
		<img class="poster" :src="details.poster" alt="" />
		<!-- titolo -->
		<h2 class="title">{{ details.title }}</h2>
		<!-- autore -->
		<h3 class="author">{{ details.author }}</h3>
		<!-- anno -->
		<span class="year">{{ details.year }}</span>
		<!-- genere -->
		<span class="genre">{{ details.genre }}</span>
	</div>
</template>

<script>
	export default {
		name: 'Album',
		props: ['details'],
	};
</script>

<style scoped lang="scss">
	@import '@/styles/vars.scss';

	.album {
		display: flex;
		flex-direction: column;
		align-items: center;
		width: calc(100% / 6 - 25px);
		min-width: 200px;
		max-width: 230px;
		padding: 25px;
		background-color: #2e3a46;
		.poster {
			height: 180px;
			// impostando la width, la differenza della dimensione delle img creva un fastidioso disallineamento sui titoli
		}
		.title {
			color: $primary-text-color;
			text-transform: uppercase;
			margin: 15px 0;
			font-size: 22px;
			text-align: center;
		}
		.year,
		.author {
			color: $secondary-text-color;
			margin: 7px 0;
		}
		.genre {
			color: $primary-text-color;
		}
		span {
			display: block;
		}
	}
</style>
