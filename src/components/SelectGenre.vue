<template>
	<select name="selectGenre" id="selectGenre">
		<option
			v-for="(value, index) in values"
			:key="index"
			@click="$emit('selectGenre', value)"
			:value="value"
			>{{ value }}</option
		>
	</select>
</template>

<script>
	export default {
		name: 'SelectGenre',
		data() {
			return {
				values: ['all', 'rock', 'pop', 'jazz', 'metal'],
			};
		},
	};
</script>

<style scoped lang="scss">
	@import '@/styles/vars.scss';

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
