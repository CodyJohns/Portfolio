<template>
	<Landing />
	<Technologies />
	<Bio />
	<Flagship @image_zoom="image_zoom" />
	<SecondBest @image_zoom="image_zoom" />
	<Projects @image_zoom="image_zoom" />
	<Other @image_zoom="image_zoom" />
	<Footer />
	<ImageZoom v-if="zoom" :imgObj="zoom_obj" :key="zoom_obj" @close="close" />
</template>

<script>
import Landing from '@/components/Landing.vue'
import Technologies from '@/components/Technologies.vue'
import Bio from '@/components/Bio.vue'
import Projects from '@/components/Projects.vue'
import Other from '@/components/Other.vue'
import Footer from '@/components/Footer.vue'
import ImageZoom from '@/components/ImageZoom.vue'
import Flagship from './components/Flagship.vue'
import SecondBest from './components/SecondBest.vue'

export default {
	name: 'App',
	components: {
		Landing,
		Technologies,
		Bio,
		Flagship,
		SecondBest,
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
	background: #fefefe;
}
</style>
