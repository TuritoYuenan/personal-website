<!-- @component Header for category pages -->

<script lang="ts">
	import Container from './Container.svelte';

	/** Header title */
	export let title: string = 'Header';
	/** Header title color */
	export let color: string = '';
</script>

<Container name="banner">
	<header>
		<h1 style:color>{title}</h1>
		<slot name="subtitle"/>
		<slot name="content" />
	</header>
</Container>

<style>
	header {
		min-height: 20vh;

		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;

		@media (max-width: 750px) {
			text-align: center;
		}
	}
</style>
