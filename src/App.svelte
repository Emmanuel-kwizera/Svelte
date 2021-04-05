<script>
	let name = "John Doe";
	let points = 100;
	let showControls = false;

	const addPoint = () => (points += 1);
	const removePoint = () => (points -= 1);
	const toggleControls = () => (showControls = !showControls)
</script>

<main>
	<div class="container">
		<div class="card">
			<h1>
				{name}
				<button class="btn" on:click={toggleControls}>+</button>
			</h1>
			<h3>{points}</h3>
			{#if showControls}
				<button class="btn" on:click={addPoint}>+1</button>
				<button class="btn btn-dark" on:click={removePoint}>-1</button>
				<input type="number" bind:value={points}>
			{/if}
		</div>
	</div>
	<!-- <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p> -->
</main>

<style>
	/* main {
	} */

	h1 {
		color: #ff3e00;
		/* text-transform: uppercase;
		font-size: 4em;
		font-weight: 100; */
	}

	h3{
		margin-bottom: 10px;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>