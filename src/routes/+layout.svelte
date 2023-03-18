<script>
	import Header from '$lib/components/Header.svelte';
	import Menu from '$lib/components/Menu.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Intro from '$lib/components/Intro.svelte';
	import Card from '$lib/components/Card.svelte';
	import './styles.css';
</script>

<div class="flex flex-col min-h-screen">
	<Header />
	<div class="flex flex-grow mb-32 mt-20 max-2xl">
		<main>
			<div class="flex-grow lg:pl-8 lg:pr-8">
				<slot />
			</div>
		</main>
	</div>
	<Footer/>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
