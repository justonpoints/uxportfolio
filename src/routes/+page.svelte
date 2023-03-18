<script>
	import Card from '$lib/components/Card.svelte';
	import Intro from '$lib/components/Intro.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>


<div class="shadow-2xl mb-5">
	<Intro/>
</div>

<section class="flex p-1 lg:p-5 m-auto">
				<div class="text-center shadow-lg bg-white w-full p-5">
					<h2 class="text-2xl">The Portfolio Feed</h2>
				</div>
				<Card date="03/17/2023" category="education" title="UX certificate from UC San Deigo Extension Complete!">
					This is content about my eduction
				</Card>
				<Card date="03/17/2023" category="social" title="Portfolio Pushed to Github">
					I pushed my portfolio to github so that you can review the code base. I used Svelete Kit and Tailwind to create the site, and i deployed it to Cloudflare.
				</Card>
				<Card date="03/01/2023" category="experience" title="Celebrating 10 years an Omniupdate / Modern Campus">
					10 Year is a long time
				</Card>
				<Card date="02/23/2023" category="skills" title="Finished LinkedIn course on Figma">
					Figma is the new black in the UX design course space, and I wanted to see what it was all about. I took a course on LinkedIn to learn basics of the UI. 
				</Card>
				<Card date="02/20/2023" category="experience" title="Released Melody Form Elements">

				</Card>
				<Card date="01/02/2023" category="design" title="Updating Netflix with Channel Surfing">
					In this project, I wondered what it would be like to take the content that exist in Netflix, and allow the user to experience it in a way similar to Television.
				</Card>

				<Card date="01/01/2023" category="design" title="What is going on with the page">
					What I am doing here is creating
				</Card>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
