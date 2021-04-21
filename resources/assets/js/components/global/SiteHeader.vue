<template>
	<header class="x-container">
		<h1 class="font-system">Site header</h1>

		<nav>
			<ul class="flex space-x-4">
				<li
					v-for="(link, index) in $props.links"
					:key="index"
				>
					<nuxt-link
						:to="link.url"
						v-text="link.title"
					/>
				</li>
			</ul>
		</nav>
	</header>
</template>

<script>
	export default {
		inheritAttrs: false,

		props: {
			links: {
				type: Array,
				default: null,
			},
		},
	};
</script>
