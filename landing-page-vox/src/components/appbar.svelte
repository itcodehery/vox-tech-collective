<script>
    import logo from "../lib/images/logo.png";

    function joinUsClick() {
        window.open("https://tally.so/r/3qRxa5", "_blank");
    }

    function scrollToAbout() {
        window.scrollTo({
            top: document.getElementById("About").offsetTop,
            behavior: "smooth",
        });
    }

    function showDialog() {
        alert(
            "Vox Technologia is a relatively new initiative. We are still working on this page. Please check back later.",
        );
    }
</script>

<div class="appbar">
    <div class="logo">
        <img src={logo} alt="logo" width="50px" height="50px" />
    </div>
    <div class="nav">
        <button class="atag" on:click={scrollToAbout}>About</button>
        <a href="/contacts">Contact</a>
        <button class="atag" on:click={showDialog}>Products</button>
    </div>
    <div>
        <button class="mainbutton" on:click={joinUsClick}>
            <p>Join Us</p>
        </button>
    </div>
</div>
