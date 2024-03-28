<script>
    let year = 2024;
    import myImage from "$lib/images/logo-white.png";

    function joinUsClick() {
        window.open("https://tally.so/r/3qRxa5", "_blank");
    }

    function goto(site) {
        window.open(site, "_blank");
    }

    function scrollToTop() {
        window.scrollTo({
            top: 0,
            behavior: "smooth",
        });
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

<footer>
    <div class="prim-wrapper">
        <div class="logo">
            <!-- add image from lib/images/logo-white.png -->
            <img src={myImage} alt="logo" width="60px" height="60px" />
            <div style="height: 1px;" />
        </div>
        <div class="sec-con-wrapper">
            <button class="main-button"
                ><a href="/" style="all: unset;">Home</a></button
            >
            <button class="text-button" on:click={scrollToAbout}>About</button>
            <button class="text-button"
                ><a href="/contacts" style="all: unset;">Contact</a></button
            >
            <button class="text-button" on:click={showDialog}>Products</button>
        </div>
    </div>
    <div class="logo">
        <div
            style="display:flex; flex-direction: column; gap: 10px; align-items: end;"
        >
            <button class="primary-button" on:click={joinUsClick}
                >Join the Community</button
            >
            <button class="primary2-button" on:click={scrollToTop}
                >Go to Top</button
            >
        </div>
        <p>&copy; {year} Vox Technologia Collective</p>
    </div>
</footer>

<style>
    footer {
        background-color: black;
        color: white;
        padding: 20px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        height: 220px;
        text-align: center;
    }

    p {
        font-size: small;
        font-family: "SFProDisplayRegular", sans-serif;
    }

    .prim-wrapper {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        gap: 20px;
    }

    .logo {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        height: auto;
    }

    .sec-con-wrapper {
        display: flex;
        flex-direction: column;
        gap: 10px;
        margin-top: 10px;
    }

    button {
        cursor: pointer;
    }

    .text-button {
        background-color: black;
        color: rgba(255, 255, 255, 0.7);
        border: none;
        font-size: 15px;
        text-align: left;
        font-family: "SFProDisplayRegular", sans-serif;
        border-radius: 60px;
        width: fit-content;
        transition: ease-in-out 0.2s;
    }

    .text-button:hover {
        background-color: #ffd5d5;
        color: black;
    }

    .text-button:active {
        transform: scale(0.9);
    }

    .main-button {
        background-color: black;
        color: white;
        border: none;
        font-size: 15px;
        text-align: left;
        font-family: "SFProDisplayBold", sans-serif;
        width: fit-content;
        border-radius: 60px;
        transition: ease-in-out 0.2s;
    }
    .main-button:hover {
        background-color: #fff3f3;
        color: black;
        padding: 6px 12px;
    }

    .main-button:active {
        transform: scale(0.95);
    }

    .primary-button {
        background-color: black;
        color: white;
        border: 2px solid rgba(255, 255, 255, 0.464);
        border-radius: 12px;
        font-size: small;
        padding: 18px 32px;
        font-family: "SFProDisplayBold", sans-serif;
        font-weight: lighter;
        letter-spacing: 0.4px;
        box-shadow: 0px 4px 4px rgba(255, 255, 255, 0.25);
        width: fit-content;
        transition: ease-in-out 0.2s;
    }

    .primary-button:hover {
        background-image: linear-gradient(120deg, #3c0808 0%, #6d0a0a 100%);
        color: white;
        transform: translate(-2px, -2px);
        box-shadow: 4px 6px 6px rgba(255, 180, 180, 0.39);
    }

    .primary-button:active {
        transform: translate(0px, 0px);
        box-shadow: 0px 0px 0px rgba(255, 255, 255, 0.25);
    }

    .primary2-button {
        background-color: black;
        color: white;
        border-radius: 12px;
        font-size: small;
        padding: 18px 32px;
        border: none;
        font-family: "SFProDisplayRegular", sans-serif;
        font-weight: lighter;
        letter-spacing: 0.4px;
        width: fit-content;
        transition: ease-in-out 0.2s;
    }

    .primary2-button:hover {
        color: rgb(255, 206, 206);
    }

    .primary2-button:active {
        transform: translate(0px, 0px);
    }

    @media (max-width: 768px) {
        .primary-button {
            padding: 12px 20px;
        }
    }
</style>
