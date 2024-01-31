<script>
    export let mainText;
    export let subText;
    function joinUsClick() {
        window.open("https://tally.so/r/3qRxa5", "_blank");
    }
</script>
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
    color: #B3E02B;
    font-weight: bold;
    letter-spacing: -0.3px;
    padding: 8px 32px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s cubic-bezier(0.075, 0.82, 0.165, 1);
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

