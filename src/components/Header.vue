<template>
	<header>
		<div class="header__container">
			<div class="menu">Menu</div>
			<div class="logo">Logo</div>
			<div class="links">Links</div>
		</div>
	</header>
</template>

<script>
	export default {
		name: 'Header'
	};
</script>

<style lang="scss" scoped>
	header {
		width: 100%;
		height: 80px;
	}
	.header__container {
		display: flex;
		justify-content: space-between;
		align-items: center;

		height: 100%;
	}

</style>