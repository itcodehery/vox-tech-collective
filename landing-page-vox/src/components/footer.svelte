<script>
    import { goto } from '$app/navigation';
    import logo from '../lib/images/logo.png';
    import { fade } from 'svelte/transition';
    const routes = [
        { name: 'Home', path: '/' },
        { name: 'Contact', path: '/contact' },
        { name: 'Products', path: '/products'},
        { name: 'Join Us', path: '/recruitment-form'},
    ];

    function navigateTo(path) {
        goto(path);
    }
</script>

<style>
    footer {
        background-color: transparent;
        color: #376200;
        font-size: smaller;
        font-family: 'Clash Display', sans-serif;
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
        color: #5ea600;
    }

    .footer-buttons {
        margin-bottom: 10px;
        background-color: transparent;
        color: #c9ff82;
        font-family: 'Clash Display';
    }

    .footer-buttons button {
        margin-right: 10px;
        background-color: transparent;
        color: #d3fd9d;
        padding: 8px 16px;
        border: none;
        cursor: pointer;
        font-size: medium;
        font-weight: normal;
        transition: fade 0.3s ease-in-out;
    }

    .footer-buttons button:hover {
        text-decoration: underline 2px;
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
            <button on:click={() => navigateTo(route.path)}>{route.name}</button>
        {/each}
    </div>
    <p>Made by Hari Prasad B K @ The Vox Technologia Collective.</p>
</footer>

