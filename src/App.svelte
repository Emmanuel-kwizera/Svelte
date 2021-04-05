<script>
	let name = "John Doe";
	let points = 100;
</script>

<main>
	<div class="container">
		<div class="card">
			<h1>{name}!</h1>
			<h3>{points}</h3>
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

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>