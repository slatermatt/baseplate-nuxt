<template>
	<div class="flex flex-col min-h-screen h-full">
		<site-header
			class="relative z-site-header"
			v-bind="$data.global"
		/>

		<main class="relative flex-auto z-site-content">
			<Nuxt />
		</main>

		<site-footer
			class="relative z-site-footer"
			v-bind="$data.global"
		/>
	</div>
</template>

<script>
	import SiteHeader from '../../assets/js/components/global/SiteHeader';
	import SiteFooter from '../../assets/js/components/global/SiteFooter';

	export default {
		components: {
			SiteHeader,
			SiteFooter,
		},

		data() {
			return {
				global: require('../../content/global.json'),
			};
		},
	};
</script>
