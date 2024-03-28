<script>
    import Detailbar from "../components/detailbar.svelte";
    import { IconVolume } from "@tabler/icons-svelte";
    import Whatwedo from "../components/whatwedo.svelte";
    import Footer from "../components/footer.svelte";
    import Appbar from "../components/appbar.svelte";
    import Accordion from "../components/accordion.svelte";

    function joinUsClick() {
        window.open("https://tally.so/r/3qRxa5", "_blank");
    }
</script>

<body>
    <section>
        <Appbar />
        <div class="section-gap" />
        <div class="actualbody">
            <h1 class="side">The Vox</h1>
            <h1>Technologia Collective</h1>
            <div class="row">
                <IconVolume color="#000" width="14px" height="14px" />
                <p>vɒks tɛknəʊləʊˈʤiːaɪeɪ</p>
            </div>
            <p class="mainp">
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
            <div class="section-gap" id="About" />
            <Whatwedo
                categoryTitle="What We Do"
                title="Things that we do in the community"
            />
            <div class="section-gap" />
            <Accordion />
            <div style="height: 100px;" />
        </div>
    </section>
    <div class="footer-border" />
</body>
<footer>
    <Footer />
</footer>

<style>
    @import "../font-import.css";
    @import "./style.css";
</style>
