<script>
	import Block from './components/Block.svelte';
	import Select from 'svelte-select';

		let items = [
			{value: 'chocolate', label: 'Chocolate'},
			{value: 'pizza', label: 'Pizza'},
			{value: 'cake', label: 'Cake'},
			{value: 'chips', label: 'Chips'},
			{value: 'ice-cream', label: 'Ice Cream'},
		];

		let selectedValue = undefined;
	export let name;

	const blocks = [0, 1, 2, 3, 4, 5];
</script>

<Select {items} bind:selectedValue></Select>
<main>
	{#each blocks as block, i}
		<div class="block">
			<h1>block {i}</h1>
			<Block/>
		</div>
	{/each}
</main>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
	}
	main {
		text-align: center;
		width: 100%;
		margin: 0 auto;
	}

	.block {
		width: 100%;
		height: 500px;
		margin-bottom: 50px;
		background-color: #f0c;
	}

	h1 {
		position: absolute;
	}

</style>
