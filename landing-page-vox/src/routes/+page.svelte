<script>
    import Detailbar from "../components/detailbar.svelte";
    import { IconVolume } from "@tabler/icons-svelte";
    import logo from "../lib/images/logo.png";
    import Whatwedo from "../components/whatwedo.svelte";
    import Contact from "../components/contact.svelte";

    const routes = [
        { name: "About", path: "/" },
        { name: "Contact", path: "/contact" },
        { name: "Products", path: "/products" },
        { name: "Join Us", path: "/recruitment-form" },
    ];

    function joinUsClick() {
        window.open("https://tally.so/r/3qRxa5", "_blank");
    }

    let expandedItem = null;

    function toggleItem(item) {
        expandedItem = expandedItem === item ? null : item;
    }

    const items = {
        "#1": {
            id: "#1",
            icon: "📚",
            title: "Have Discussions on Tech and its impact on the community",
            content:
                "We have discussions on various topics in tech and how it impacts the community. We discuss the latest trends and how we can contribute to the community.",
        },
        "#2": {
            id: "#2",
            icon: "🛠️",
            title: "Work on Projects together and build portfolios of each other",
            content:
                "We work on projects together and build portfolios of each other. We help each other grow and learn new skills.",
        },
        "#3": {
            id: "#3",
            icon: "🎉",
            title: "Have fun and learn together in a safe environment",
            content:
                "We have fun and learn together in a safe environment. We make sure that everyone is comfortable and has a good time.",
        },
    };
</script>

<body>
    <section>
        <div class="appbar">
            <div class="logo">
                <img src={logo} alt="logo" width="50px" height="50px" />
            </div>
            <div class="nav">
                <a href="/">About</a>
                <a href="/">Contact</a>
                <a href="/">Products</a>
            </div>
            <div>
                <button class="mainbutton" on:click={joinUsClick}>
                    <p>Join Us</p>
                </button>
            </div>
        </div>
        <div class="section-gap" />
        <div class="actualbody">
            <h1 class="side">The Vox</h1>
            <h1>Technologia Collective</h1>
            <div class="row">
                <IconVolume color="#000" width="14px" height="14px" />
                <p>vɒks tɛknəʊləʊˈʤiːaɪeɪ</p>
            </div>
            <p>
                A student-driven community based in Bangalore, In, dedicated to
                helping college students collaborate on tech-related projects,
                learn new skills, and network with fellow students.
            </p>
            <Detailbar
                buttonText="Join Us"
                subtitle="members in our community. Even more to come."
                title="23"
                value="23"
                buttonAction={joinUsClick}
            />
            <div class="section-gap" />
            <Whatwedo
                categoryTitle="What We Do"
                title="Things that we do in the community"
            />
            <div class="section-gap" />
            <div class="text">
                <p style="color: blue;">What are we hoping for</p>
                <h1>Aims</h1>
            </div>
            <div class="accordion">
                {#each Object.values(items) as yoooo}
                    <div class="accordion-item">
                        <button
                            class="accordion-header"
                            on:click={() => toggleItem(yoooo.id)}
                        >
                            <div class="titleheader">
                                <p>{yoooo.icon}</p>
                                <p>{yoooo.title}</p>
                                {expandedItem === yoooo.id ? "▲" : "▼"}
                            </div>

                            <div
                                class="accordion-content"
                                style={expandedItem === yoooo.id
                                    ? ""
                                    : "display: none;"}
                            >
                                {yoooo.content}
                            </div>
                        </button>
                    </div>
                {/each}
            </div>
            <Contact />
            <div style="height: 100px;" />
        </div>
    </section>
</body>

<style>
    @import "../font-import.css";

    section {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .row {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 10px;
        margin-top: 10px;
    }

    .row p {
        margin: 0;
    }

    .appbar {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        width: 100%;
        background-color: transparent;
        padding-top: 10px;
        padding-bottom: 10px;
        color: #fff;
    }

    .text {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        gap: 10px;
        margin-bottom: 20px;
    }

    .logo {
        display: flex;
        flex-direction: row;
        margin-left: 10px;
        align-items: center;
        justify-content: center;
    }

    .nav {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        background-color: rgba(0, 0, 0, 0.122);
        border-radius: 80px;
        gap: 10px;
        font-family: "SFProDisplayRegular", sans-serif;
    }

    .nav a {
        color: #000;
        font-size: 14px;
        text-decoration: none;
        border-radius: 80px;
        padding: 10px;
        transition: ease-in 0.2s;
    }

    .nav a:hover {
        background-color: #0000003f;
    }

    .mainbutton {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        background-color: #000;
        font-family: "Raleway", sans-serif;
        color: #fff;
        padding: 10px;
        margin-right: 10px;
        max-height: 40px;
        border: none;
        border-radius: 80px;
        cursor: pointer;
    }

    .mainbutton:hover {
        background-color: #000000d7;
    }

    .mainbutton p {
        margin-left: 10px;
        margin-right: 10px;
    }

    h1 {
        font-family: "YoungSerif", sans-serif;
        font-size: 40px;
        margin: 0;
    }

    .side {
        color: rgba(0, 0, 0, 0.334);
    }

    p {
        font-family: "SFProDisplayRegular", sans-serif;
        font-size: 16px;
        margin: 0;
    }
    .section-gap {
        height: 100px;
    }

    .actualbody {
        display: flex;
        flex-direction: column;
        gap: 0px;
    }

    .accordion {
        display: flex;
        flex-direction: column;
        align-self: center;
        align-items: center;
        justify-content: center;
        gap: 10px;
        width: 100%;
        max-width: 500px;
        color: black;
    }

    .accordion-item {
        display: flex;
        flex-direction: row;
        font-family: "SFProDisplayRegular", sans-serif;
        background-color: #fff;
        border: 1px solid #ccc;
        border-radius: 8px;
        width: 100%;
    }

    .accordion-header {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        padding: 10px;
        font-family: "SFProDisplayBold", sans-serif;
        background-color: #f5f5f5;
        border-bottom: 1px solid #ccc;
        border-radius: 8px 8px 0 0;
        cursor: pointer;
        transition: ease-in-out 0.2s;
        width: 100%;
    }

    .titleheader {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        width: 100%;
    }

    .accordion button {
        background: none;
        border: none;
        cursor: pointer;
    }

    .accordion-content {
        border-top: 1px solid #fff;
        padding: 4px;
        margin-top: 10px;
        border: dashed 1px #a8a8a8;
        border-radius: 0 0 8px 8px;
        transition: ease-in-out 0.2s;
        text-align: left;
        font-family: "SFProDisplayRegular", sans-serif;
    }
</style>
