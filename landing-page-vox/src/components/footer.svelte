<script>
    import { goto } from "$app/navigation";
    import { IconDoorExit } from "@tabler/icons-svelte";
    import logo from "../lib/images/logo.png";
    const routes = [
        { name: "Home", path: "/" },
        { name: "Contact", path: "/contact" },
        { name: "Products", path: "/products" },
        { name: "About", path: "/about" },
        { name: "Join Us", path: "/recruitment-form" },
    ];

    function navigateTo(path) {
        goto(path);
    }

    function joinUsClick() {
        window.open("https://tally.so/r/3qRxa5", "_blank");
    }
</script>

<footer>
    <div class="head">
        <a href="/"><img src={logo} alt="logo" width="80px" height="80px" /></a>
        <div style="margin-left: 10px;"></div>
        <p>Since November 2023</p>
    </div>
    <div class="footer-buttons">
        {#each routes as route}
            {#if route.name === "Join Us"}
                <button on:click={joinUsClick}>Join Us</button>
            {:else if route.name === "Products"}
                <!-- make an alert -->
                <button
                    on:click={() =>
                        alert(
                            "Vox Technologia is a relatively young initiative.\nWait some time to see products from us.",
                        )}>{route.name}</button
                >
            {:else}
                <button on:click={() => navigateTo(route.path)}
                    >{route.name}</button
                >
            {/if}
        {/each}
    </div>
    <p>Made by Hari Prasad @ The Vox Technologia Collective.</p>
    <div class="startup">
        <p>Check out our latest startup project: Studvisor</p>
        <button>To Studvisor</button>
        <button><IconDoorExit color="#fff" width="24px" /></button>
    </div>
</footer>

<style>
    footer {
        background-color: transparent;
        color: #557b23;
        font-size: smaller;
        font-family: "Raleway", sans-serif;
        font-weight: bold;
        letter-spacing: -0.3px;
        padding: 20px;
        border-radius: 8px;
        text-align: center;
        align-items: center;
        justify-content: center;
        align-self: center;
    }

    .head {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-self: center;
        align-items: center;
        color: #c9ff82;
    }

    .footer-buttons {
        display: flex;
        align-items: center;
        justify-content: center;
        align-items: center;
        align-self: center;
        margin-bottom: 10px;
        background-color: transparent;
        color: #c9ff82;
    }

    @media (max-width: 600px) {
        .footer-buttons {
            flex-wrap: wrap;
        }
    }

    .footer-buttons button {
        background-color: transparent;
        color: #d3fd9d;
        padding: 8px 16px;
        border: none;
        border-radius: 6px;
        font-size: small;
        font-family: "Raleway";
        font-weight: bold;
        cursor: pointer;
        font-weight: bold;
        transition:
            background-color 0.15s ease-in,
            color 0.15s ease-in,
            transform 0.15s ease-in;
    }

    .footer-buttons button:hover {
        background-color: #c9ff82;
        color: #557b23;
        transform: translate(-3px, -3px);
        border-bottom: 5px solid #557b23;
        border-right: 5px solid #557b23;
    }

    .footer-buttons button:active {
        transform: translate(0px, 0px);
        border-bottom: 0px;
        border-right: 0px;
    }

    .startup {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        align-self: center;
        margin-top: 20px;
        background-color: white;
        color: #c9ff82;
        gap: 10px;
    }

    .startup button {
        background-color: transparent;
        color: #273d0b;
        padding: 8px 16px;
        border: none;
        border-radius: 6px;
        font-size: small;
        font-family: "Raleway";
        font-weight: bold;
        cursor: pointer;
        font-weight: bold;
        transition:
            background-color 0.15s ease-in,
            color 0.15s ease-in,
            transform 0.15s ease-in;
    }
</style>
