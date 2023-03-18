<svelte:head>
	<title>Test</title>
	<meta name="description" content="This is a test page" />
</svelte:head>

<script>
	import DesignCard from '$lib/components/DesignCard.svelte';
	import surf from '$lib/images/surf.png';
	import vote from '$lib/images/votenow.jpg';
</script>

<div class="text-column">
	<div class="section">
        <div class="columns is-multiline is-centered">
        <div class="column is-half is-centered">
            <a href="https://rdwkn5.axshare.com/" target="_blank" title="Open Netflix project">
            <DesignCard title="Netflix Surfing" img="{surf}" desc="What habits can we borrow from Netflix to make watching its content more passive. In this design I expore adding a random or surf mode to Netflix." />
            </a>
        </div>
        <div class="column is-half">
            <a href="https://q23yz8.axshare.com/" target="_blank" title="open election mart project">
            <DesignCard title="Election Mart" img="{vote}" desc="Voting in person and by mail is inefficient. Also, it is difficult to know what is on the ballot, and be informed about all the choices. This design explores what an election site might look like." />
            </a>
        </div>
    </div>
    </div>
</div>
