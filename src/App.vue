<template>
	<Landing></Landing>
	<Technologies></Technologies>
	<Bio></Bio>
	<Projects @image_zoom="image_zoom"></Projects>
	<Other @image_zoom="image_zoom"></Other>
	<Footer></Footer>
	<ImageZoom v-if="zoom" :imgObj="zoom_obj" :key="zoom_obj" @close="close"></ImageZoom>
</template>

<script>
import Landing from '@/components/Landing.vue'
import Technologies from '@/components/Technologies.vue'
import Bio from '@/components/Bio.vue'
import Projects from '@/components/Projects.vue'
import Other from '@/components/Other.vue'
import Footer from '@/components/Footer.vue'
import ImageZoom from '@/components/ImageZoom.vue'

export default {
	name: 'App',
	components: {
		Landing,
		Technologies,
		Bio,
		Projects,
		Other,
		Footer,
		ImageZoom
	},
	data: function() {
		return {
			zoom: false,
			zoom_obj: null,
		}
	},
	created() {
		document.title = "Cody Johns' Portfolio";
	},
	methods: {
		image_zoom(obj) {
			this.zoom_obj = obj;
			this.zoom = true;
		},
		close(bool) {
			this.zoom = bool;
		}
	}
}
</script>

<style>
body {
	width: 100% !important;
}

#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	background: #F9F4F5;
}
</style>
