<script>
    import { onMount, afterUpdate, onDestroy } from 'svelte';

    export let mainText;
    export let subText;
    let isMobile = false;

    function joinUsClick() {
        window.open('https://tally.so/r/3qRxa5', '_blank');
    }

    function checkScreenWidth() {
        isMobile = window.innerWidth < 600;
    }

    onMount(() => {
        checkScreenWidth();

        window.addEventListener('resize', checkScreenWidth);

        afterUpdate(() => {
            checkScreenWidth();
        });

        onDestroy(() => {
            window.removeEventListener('resize', checkScreenWidth);
        });
    });
</script>

<!-- if it's a mobile screen, render this on the screen -->
{#if isMobile}
    <div class="main-card">
        <h1>{mainText}</h1>
        <p>{subText}</p>
        <button on:click={joinUsClick}>Join Us</button>
    </div>
{:else}
    <div class="main-card">
        <h1>{mainText}</h1>
        <p>{subText}</p>
        <button on:click={joinUsClick}>Join Us</button>
    </div>
{/if}

<style>
	.main-card {
		background-color: #aed340;
		background-image: url('../lib/images/primaryCardbg.png');
		background-size: cover;
		color: #111111;
		align-self: center;
		padding: 112px;
		display: flex;
		align-items: center;
		flex-direction: column;
		border-radius: 8px;
		text-align: center;
	}

	.main-card h1 {
		margin: 0;
		padding-bottom: 0px;
		font-size: 36px;
		letter-spacing: -0.3px;
		font-weight: bold;
	}

	@media screen and (max-width: 600px) {
		.main-card {
			padding: 32px;
			align-items: center;
			background-color: #aed340;
			background-image: url('../lib/images/primaryCardbg.png');
			background-size: cover;
			color: #000;
			align-self: center;
			text-align: center;
			display: flex;
			align-items: center;
			flex-direction: column;
			border-radius: 8px;
		}

		.main-card h1 {
			font-size: 20px;
		}

		.main-card p {
			font-size: 6px;
		}
	}

	.main-card p {
		color: #134700;
		font-size: 18px;
		font-weight: 500;
		margin-bottom: 10px;
	}

	.main-card button {
		background-color: rgb(46, 60, 0);
		color: #b3e02b;
		font-weight: bold;
		letter-spacing: -0.3px;
		padding: 8px 32px;
		border: none;
		border-radius: 4px;
		cursor: pointer;
		transition: background-color 0.3s ease-in;
	}

	.main-card button:hover {
		background-color: transparent;
		border: #222d00 2px solid;
		padding: 6.3px 30px;
		border-style: dashed;
		color: #222d00;
	}
</style>
