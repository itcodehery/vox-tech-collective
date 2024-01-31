<script>
    import logo from '../lib/images/logo.png';
    export let search;
    export let showNameBar = false;
    export let showJoinUsButton = true;
    export let formAppBar = false;
    function joinUsClick() {
        window.open("https://tally.so/r/3qRxa5", "_blank");
    }
</script>
<style>
    @import '../font-import.css';
    /* if its a web screen use this style */
    .app-bar {
        position: fixed;
        top: 5%;
        left: 50%;
        transform: translate(-50%, -50%);
        background-color: rgba(0,0,0,0.3);
        backdrop-filter: blur(10px);
        -webkit-backdrop-filter: blur(10px);
        background-image: url('../lib/images/secondaryCardbg.png');
        background-size: 20in;
        background-position: right;
        color: #b3e02b;
        align-self: center;
        width: 60%;
        height: 18px;
        padding: 16px;
        display: flex;
        align-items: center;
        justify-content: space-between  ;
        border-radius: 8px;
        border: #d4ea9948 1px solid;
        /* z-index: 1; */
    }

    .app-bar-2 {
        position: fixed;
        top: 5%;
        left: 50%;
        transform: translate(-50%, -50%);
        background-color: rgba(0,0,0,0.3);
        backdrop-filter: blur(10px);
        -webkit-backdrop-filter: blur(10px);
        background-image: url('../lib/images/secondaryCardbg.png');
        background-size: 20in;
        background-position: right;
        color: #b3e02b;
        align-self: center;
        width: 60%;
        height: 18px;
        padding: 16px;
        display: none;
        align-items: center;
        justify-content: space-between  ;
        border-radius: 8px;
        border: #d4ea9948 1px solid;
        /* z-index: 1; */
    }
    
    /* if its a mobile screen, use this */
    @media screen and (max-width: 600px) {
        .app-bar {
            width: 80%;
            height: 18px;
            padding: 16px;
            display: none;
            align-items: center;
            justify-content: space-between  ;
            border-radius: 8px;
            border: #d4ea9948 1px solid;
            /* z-index: 1; */
        }

        .app-bar-2 {
            width: 80%;
            height: 18px;
            padding: 16px;
            display: flex;
            align-items: center;
            justify-content: space-between  ;
            border-radius: 8px;
            border: #d4ea9948 1px solid;
        }
    }

    .container {
        display: flex;
        align-items: center;
        gap: 10px;
    }

    .app-bar .container a {
        display: flex;
        align-items: center;
        text-decoration: none;
    }

    .primary-button {
    margin-left: auto;
    background-color: rgba(191, 255, 0, 0.65);
    color: #1c3700;
    text-transform: capitalize;
    font-weight: bold;
    padding: 8px 16px;
    font-family: 'Raleway';
    font-size: bold;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    position: sticky;
    float: right;
    transition: background-color 0.3s ease-in-out;
  }

  .inputbar {
    background-color: rgba(40, 53, 0, 0.5);
    color: #87aa1d;
    text-transform: capitalize;
    padding: 8px 16px;
    border: none;
    height: 20px;
    border-radius: 4px;
    cursor: pointer;
    /* width: 100%; */
  }

  .secondary-button {
    margin-left: auto;
    background-color: transparent;
    color: #b3e02b;
    text-transform: capitalize;
    font-size: small;
    font-weight: normal;
    font-family: 'Raleway';
    padding: 8px 16px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s ease-in-out;
  }

  .container-two {
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .app-bar button:hover {
    background-color: #1c3700;
    color: #B3E02B;
  }
</style>

<!-- if its a mobile screen, use this -->

<header class="app-bar">
    {#if !formAppBar}
    <div class="container">
        <!-- add link to home page to the image using <a> tag -->
        <a href="/"><img src="{logo}" href= "/" alt="logo" width="42px" height="42px"/></a>
        {#if showNameBar==true}
        <input class= "inputbar" bind:value = {search} type="text" placeholder="Enter your Name" />
        {/if}
    </div>
    <div class = "container">
        <a href="/contact/"><button class="secondary-button">Contact</button></a>
        {#if showJoinUsButton==true}
        <button class="primary-button" on:click={joinUsClick}>Join Us</button>
        {/if}
    </div>
    {:else}
    <div class="container-two">
        <a href="/"><img src="{logo}" href= "/" alt="logo" width="42px" height="42px"/></a>
    </div>
    {/if}

</header>

<header class="app-bar-2">
    <div class="container-two">
        <!-- add link to home page to the image using <a> tag -->
        <a href="/"><img src="{logo}" href= "/" alt="logo" width="42px" height="42px"/></a>
    </div>
    {#if showJoinUsButton==true}
        <button class="primary-button" on:click={joinUsClick}>Join Us</button>
    {/if}
</header>