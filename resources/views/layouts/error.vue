<template>
	<div class="x-container">
		<p>{{ $props.error.statusCode }} - {{ $props.error.message }}</p>
	</div>
</template>

<script>
	export default {
		props: {
			error: {
				type: Object,
				default: null,
			},
		},

		head() {
			return {
				title: this.$props.error.statusCode,
			};
		},
	};
</script>
