<template>
	<div id="app">
		<AlbumList />
	</div>
</template>

<script>
	import AlbumList from '@/components/AlbumList';

	export default {
		name: 'App',
		components: {
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
</style>
