<template>
	<div id="app">
		<Header />
		<AlbumList />
	</div>
</template>

<script>
	import Header from '@/components/Header';
	import AlbumList from '@/components/AlbumList';

	export default {
		name: 'App',
		components: {
			Header,
			AlbumList,
		},
	};
</script>

<style lang="scss">
	* {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}

	.container {
		max-width: 1600px;
		margin: 0 auto;
	}
</style>
