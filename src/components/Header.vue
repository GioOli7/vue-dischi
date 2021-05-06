<template>
	<header>
		<div class="container">
			<img src="@/assets/logo.png" alt="" />
		</div>
	</header>
</template>

<script>
	export default {
		name: 'Header',
	};
</script>

<style scoped lang="scss">
	@import '@/styles/vars.scss';

	header {
		padding: 10px 0;
		background-color: $light-blue;
	}

	.container {
		display: flex;
		align-items: center;
	}

	img {
		max-width: 50px;
		padding-left: 15px;
	}
</style>
