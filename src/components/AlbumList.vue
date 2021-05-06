<template>
	<div class="content">
		<div class="container">
			<div class="album-list" v-if="loaded">
				<Album v-for="(album, index) in albums" :key="index" :details="album" />
			</div>
			<img v-else class="loading-logo" src="@/assets/logo.png" alt="" />
		</div>
	</div>
</template>

<script>
	import axios from 'axios';
	import Album from '@/components/Album';

	export default {
		name: 'AlbumList',
		components: {
			Album,
		},
		data() {
			return {
				// my data
				albums: [],
				loaded: false,
			};
		},
		created() {
			this.getAlbums();
		},
		methods: {
			// my methods
			getAlbums() {
				axios
					.get('https://flynn.boolean.careers/exercises/api/array/music')
					.then(result => {
						this.albums = result.data.response;
						this.loaded = true;
					})
					.catch(error => console.log(error));
			},
		},
	};
</script>

<style scoped lang="scss">
	.container {
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.album-list {
		padding-top: 50px;
		padding-bottom: 20px;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 30px;
	}

	.loading-logo {
		max-width: 40%;
		opacity: 0.3;
	}
</style>
