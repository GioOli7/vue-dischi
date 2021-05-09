<template>
	<div class="select">
		<label>Filter by genre</label>
		<select
			name="selectGenre"
			id="selectGenre"
			v-model="value"
			@change="$emit('selectGenre', value)"
		>
			<option v-for="(value, index) in genres" :key="index" :value="value">{{ value }}</option>
		</select>
	</div>
</template>

<script>
	export default {
		name: 'SelectGenre',
		props: ['genres'],
		data() {
			return {
				value: 'all',
			};
		},
	};
</script>

<style scoped lang="scss">
	@import '@/styles/vars.scss';

	label {
		color: white;
		margin-right: 10px;
	}

	select {
		background-color: #2e3a46;
		border: 1px solid rgba(255, 255, 255, 0.1);
		padding: 10px;
		color: white;
		font-weight: bold;
		width: 120px;
		height: 40px;
	}
</style>
