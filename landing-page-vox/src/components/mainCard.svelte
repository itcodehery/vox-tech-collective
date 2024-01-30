<script>
    export let mainText;
    export let subText;
    function joinUsClick() {
        window.open("https://tally.so/r/3qRxa5", "_blank");
    }
</script>
<style>
    .main-card {
        background-color: #B3E02B;
        background-image: url('../lib/images/primaryCardbg.png');
        background-size: cover;
        color: #000;
        align-self: center;
        padding: 112px;
        display: flex;
        align-items: center;
        flex-direction: column;
        border-radius: 8px;
    }
    

    .main-card h1 {
        margin: 0;
        font-size: 42px;
        font-weight: bold;
    }

    @media screen and (max-width: 600px) {
        .main-card {
            padding: 32px;
            align-items: center;
        }

        .main-card h1 {
            font-size: 24px;
        }

        .main-card p {
            font-size: 10px;
        }
    }

    .main-card p {
        color: #134700;
        font-size: 24px;
        font-weight: 500;
        margin-bottom: 10px;
    }

    .main-card button {
    background-color: rgb(46, 60, 0);
    color: #B3E02B;
    text-transform: capitalize;
    font-family: 'Clash Display';
    font-weight: bold;
    padding: 8px 32px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }

  .main-card button:hover {
    background-color: transparent;
    border: #222d00 2px solid;
    padding: 6.5px 30px;
    border-style: dashed;
    color: #222d00;
  }
</style>

<!-- if its a mobile screen, render this on the screen -->
{#if window.innerWidth < 600}
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

