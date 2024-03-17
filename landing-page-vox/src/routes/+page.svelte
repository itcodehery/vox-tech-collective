<script>
    import Detailbar from "../components/detailbar.svelte";
    import { IconVolume } from "@tabler/icons-svelte";
    import logo from "../lib/images/logo.png";
    import Whatwedo from "../components/whatwedo.svelte";

    const routes = [
        { name: "Home", path: "/" },
        { name: "Contact", path: "/contact" },
        { name: "Products", path: "/products" },
        { name: "About", path: "/about" },
        { name: "Join Us", path: "/recruitment-form" },
    ];

    function joinUsClick() {
        window.open("https://tally.so/r/3qRxa5", "_blank");
    }
</script>

<body>
    <section>
        <div class="appbar">
            <div class="logo">
                <img src={logo} alt="logo" width="50px" height="50px" />
            </div>
            <div class="nav">
                <a href="/">Home</a>
                <a href="/contact">Contact</a>
                <a href="/products">Products</a>
                <a href="/about">About</a>
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
                buttonAction=""
                buttonText="Join Us"
                subtitle="members in our community. Even more to come."
                title="23"
                value="23"
            />
            <div class="section-gap" />
            <Whatwedo
                categoryTitle="What We Do"
                title="Things that we do in the community"
            />
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
        font-family: "SFProDisplayBold", sans-serif;
        font-size: 40px;
        margin: 0;
    }

    .side {
        color: rgba(0, 0, 0, 0.334);
    }

    p {
        font-family: "SFProDisplayRegular", sans-serif;
        font-size: 16px;
    }
    .section-gap {
        height: 100px;
    }

    .actualbody {
        display: flex;
        flex-direction: column;
        gap: 0px;
    }
</style>
