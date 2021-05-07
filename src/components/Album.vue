<template>
	<div class="content">
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

	.content {
		display: flex;
		flex-direction: column;
		.poster {
			height: 170px;
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
			text-align: center;
		}
		.genre {
			color: $primary-text-color;
			text-align: center;
		}
		span {
			display: block;
		}
	}
</style>
