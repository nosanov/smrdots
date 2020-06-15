<template>
	<div id="gallery__area">
		It's {{text}}
	</div>
</template>

<script>
	export default {
		name: 'GalleryArea',
		data() {
			return {
				text: 'Gallery Area'
			}
		}
	};
</script>

<style lang="scss" scoped>
	#gallery__area {
		position: fixed;
		top: 35%;
		left: 40%;
	}
</style>