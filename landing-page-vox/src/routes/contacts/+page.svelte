<script>
    import Contact from "../../components/contact.svelte";
    import logo from "$lib/images/logo.png";
    import Footer from "../../components/footer.svelte";
    function joinUsClick() {
        window.open("https://tally.so/r/3qRxa5", "_blank");
    }
</script>

<body>
    <div class="appbar">
        <div class="logo">
            <img src={logo} alt="logo" width="50px" height="50px" />
        </div>
        <div class="nav">
            <a href="/">About</a>
            <a href="/" class="homea">Home</a>
            <a href="/">Products</a>
        </div>
        <div>
            <button class="mainbutton" on:click={joinUsClick}>
                <p>Join Us</p>
            </button>
        </div>
    </div>
    <section>
        <Contact />
    </section>
    <div style="height: 100px;" />
    <div class="footer-border" />
</body>
<footer>
    <Footer />
</footer>

<style>
    @import "../style.css";

    .homea {
        font-family: "SFProDisplayBold", sans-serif;
    }
</style>
