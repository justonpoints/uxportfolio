<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';
</script>

<header class="w-full h-18 bg-black text-white text-xl fixed top-0 flex flex-row">
	<div class="flex-grow p-5">JUSTON'S PORTFOLIO</div> 
	<div>
		<ul class="style-none flex flex-row mr-16">
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li aria-current={$page.url.pathname === '/experience' ? 'page' : undefined}>
				<a href="/experience">Experience</a>
			</li>
			<li aria-current={$page.url.pathname === '/education' ? 'page' : undefined}>
				<a href="/education">Education</a>
			</li>
			<li aria-current={$page.url.pathname === '/skills' ? 'page' : undefined}>
				<a href="/skills">Skills</a>
			</li>
			<li aria-current={$page.url.pathname === '/designs' ? 'page' : undefined}>
				<a href="/designs">Designs</a>
			</li>
			<li aria-current={$page.url.pathname === '/social' ? 'page' : undefined}>
				<a href="/social">Social</a>
			</li>
		</ul>
	</div>
</header>

<style>
	li[aria-current='page']{
		@apply bg-white text-black;
	}

	li a{
		@apply block p-5;
	}
</style>
