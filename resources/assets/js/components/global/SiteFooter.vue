<template>
	<footer class="x-container w-full">
		<ul class="flex space-x-4">
			<li
				v-for="(link, index) in $props.social"
				:key="index"
			>
				<a
					:href="link.url"
					v-text="link.title"
				/>
			</li>
		</ul>

		<p>
			&copy; <span v-text="$data.year" />
		</p>
	</footer>
</template>

<script>
	export default {
		inheritAttrs: false,

		props: {
			social: {
				type: Array,
				default: null,
			},
		},

		data() {
			return {
				year: new Date().getFullYear(),
			};
		},
	};
</script>
