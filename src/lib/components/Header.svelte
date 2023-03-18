<script>
	import { page } from '$app/stores';
	import Fa from 'svelte-fa/src/fa.svelte'
    import {faXmark,faHamburger,faCompassDrafting,faShareNodes, faGraduationCap, faArrowUpRightFromSquare, faBriefcase, faUserNinja } from '@fortawesome/free-solid-svg-icons'
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';

	$:showMenu = false;

	function toggleMenu(){
		showMenu = !showMenu;
	}
</script>

<header class="w-full h-18 bg-black text-white text-xl fixed top-0 flex flex-row">
	<div class="flex-grow p-5">PORTFOLIO</div> 
	<div class="hidden md:block">
		<ul class="style-none flex flex-row flex-wrap lg:mr-16 lg:text-lg text-sm">
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li aria-current={$page.url.pathname === '/experience' ? 'page' : undefined}>
				<a href="/experience"><Fa class="inline" icon={faBriefcase} /> Experience</a>
			</li>
			<li aria-current={$page.url.pathname === '/education' ? 'page' : undefined}>
				<a href="/education"><Fa class="inline" icon={faGraduationCap} /> Education</a>
			</li>
			<li aria-current={$page.url.pathname === '/skills' ? 'page' : undefined}>
				<a href="/skills"><Fa class="inline" icon={faUserNinja} /> Skills</a>
			</li>
			<li aria-current={$page.url.pathname === '/designs' ? 'page' : undefined}>
				<a href="/designs"><Fa class="inline" icon={faCompassDrafting} /> Designs</a>
			</li>
			<li aria-current={$page.url.pathname === '/social' ? 'page' : undefined}>
				<a href="/social"><Fa class="inline" icon={faShareNodes} /> Social</a>
			</li>
		</ul>
	</div>
	<div>
		<button on:click={toggleMenu} class="text-white text-3xl p-5 md:hidden">
			{#if showMenu===true}
				<Fa class="inline" icon={faXmark} /><span class="sr-only">Close Navigation Menu</span>
			{:else}
				<Fa class="inline" icon={faHamburger} /><span class="sr-only">Open Navigation Menu</span>
			{/if}
		</button>
		<div class="{showMenu ? "flex" : "hidden"} fixed top-20 left-0 z-20 bg-black w-full justify-items-center items-center p-5">
			<ul class="style-none flex flex-col justify-items-center items-center w-full h-full text-white text-3xl">
				<li class="w-full p-2" aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
					<a on:click={toggleMenu} href="/">Home</a>
				</li>
				<li class="w-full p-2" aria-current={$page.url.pathname === '/experience' ? 'page' : undefined}>
					<a on:click={toggleMenu} href="/experience"><Fa class="inline" icon={faBriefcase} /> Experience</a>
				</li>
				<li class="w-full p-2" aria-current={$page.url.pathname === '/education' ? 'page' : undefined}>
					<a on:click={toggleMenu} href="/education"><Fa class="inline" icon={faGraduationCap} /> Education</a>
				</li>
				<li class="w-full p-2" aria-current={$page.url.pathname === '/skills' ? 'page' : undefined}>
					<a on:click={toggleMenu} href="/skills"><Fa class="inline" icon={faUserNinja} /> Skills</a>
				</li>
				<li class="w-full p-2" aria-current={$page.url.pathname === '/designs' ? 'page' : undefined}>
					<a on:click={toggleMenu} href="/designs"><Fa class="inline" icon={faCompassDrafting} /> Designs</a>
				</li>
				<li class="w-full p-2" aria-current={$page.url.pathname === '/social' ? 'page' : undefined}>
					<a on:click={toggleMenu} href="/social"><Fa class="inline" icon={faShareNodes} /> Social</a>
				</li>
			</ul>
		</div>
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
