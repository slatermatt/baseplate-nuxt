<template>
	<div class="x-container">
		<pre v-text="$data" />
	</div>
</template>

<script>
	import head from '../../assets/js/mixins/head';

	export default {
		mixins: [head],

		async asyncData ({ $content }) {
			return await $content('index').fetch();
		},
	};
</script>
