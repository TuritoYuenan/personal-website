<!-- @component Two parallel contents, responsively collapse on small width -->

<script lang="ts">
	export let flip: boolean = false;
</script>

<section style:direction={flip ? 'rtl' : ''}>
	<slot name="one">
		<p>Lorem ipsum dolor sit amet</p>
	</slot>
	<slot name="two">
		<p>Lorem ipsum dolor sit amet</p>
	</slot>
</section>

<style>
	section {
		padding: 1rem;
		display: grid;
		gap: 1rem;

		@media (min-width: 700px) {
			grid-template-columns: repeat(2, 1fr);
		}
	}
</style>
