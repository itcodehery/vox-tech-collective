<script>
    import { goto } from '$app/navigation';
    import logo from '../lib/images/logo.png';
    const routes = [
        { name: 'Home', path: '/' },
        { name: 'Contact', path: '/contact' },
        { name: 'Products', path: '/products'},
        { name: 'Join Us', path: '/recruitment-form'},
    ];

    function navigateTo(path) {
        goto(path);
    }

    function joinUsClick() {
        window.open("https://tally.so/r/3qRxa5", "_blank");
    }
</script>

<style>
    footer {
        background-color: transparent;
        color: #557b23;
        font-size: smaller;
        font-family: 'Raleway', sans-serif;
        font-weight: bold;
        letter-spacing: -0.3px;
        padding: 20px;
        border-radius: 8px;
        text-align: left;
        align-self: flex-end;
    }

    .head {
        display: flex;
        flex-direction: row;
        justify-content: start;
        align-items: center;
        color: #c9ff82;
    }

    .footer-buttons {
        margin-bottom: 10px;
        background-color: transparent;
        color: #c9ff82;
    }

    .footer-buttons button {
        margin-right: 10px;
        background-color: transparent;
        color: #d3fd9d;
        padding: 8px 16px;
        border: none;
        border-radius: 6px;
        font-size: small;
        font-family: 'Raleway';
        font-weight: bold;
        cursor: pointer;
        font-weight: normal;
        transition: background-color 0.3s ease-in;
    }

    .footer-buttons button:hover {
        background-color: #c9ff82;
        color: #557b23;
        font-weight: bold;
    }
</style>

<footer>
    <div class="head">
        <a href='/'><img src={logo} alt="logo" width="80px" height="80px"/></a>
        <div style="margin-left: 10px;"></div>
        <p>Since November 2023</p>
    </div>
    <div class="footer-buttons">
        {#each routes as route}
            {#if route.name === 'Join Us'}
                <button on:click={joinUsClick}>Join Us</button>
            {:else}
                <button on:click={() => navigateTo(route.path)}>{route.name}</button>
            {/if}
        {/each}
    </div>
    <p>Made by Hari Prasad B K @ The Vox Technologia Collective.</p>
</footer>

