<script>
	export let name;
	import { Router, Route } from 'svelte-routing';
	import Navbar from './components/Navbar.svelte';
	import Footer from './components/Footer.svelte';
	import Home from './routes/Home.svelte';
	// Import other pages and components
</script>

<main>
	<Navbar />
	<Router>
		<Route path="/" component="{Home}"/>
		/* Define other paths here */
	</Router>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<Footer />
</main>

<style>
	/* Global and specific styles */
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>