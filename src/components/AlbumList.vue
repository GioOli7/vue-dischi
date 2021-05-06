<template>
	<div>
		<Album v-for="(album, index) in albums" :key="index" :details="album" />
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
			};
		},
		created() {
			this.getAlbums();
		},
		methods: {
			// my methods
			getAlbums() {
				axios
					.get(
						'https://flynn.boolean.careers/exercises/api/array/music'
					)
					.then((result) => {
						this.albums = result.data.response;
					})
					.catch((error) => {
						console.log(error);
					});
			},
		},
	};
</script>

<style></style>
