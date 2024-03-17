<script>
    import logo from "../lib/images/logo.png";

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
                <button class="mainbutton">
                    <p>Join Us</p>
                </button>
            </div>
        </div>
        <div class="section-gap" />
        <div class="actualbody">
            <h1 class="side">The Vox</h1>
            <h1>Technologia Collective</h1>
            <p>vɒks tɛk nəʊ ləʊ ˈʤiːˈaɪ eɪ</p>
            <p>
                We are always looking for talented individuals to join our team.
                If you are interested in working with us, please fill out the
                form below and we will get back to you as soon as possible.
            </p>
            <button on:click={joinUsClick} class="mainbutton">
                <p>Join Us</p>
            </button>
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
