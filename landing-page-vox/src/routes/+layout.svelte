<script>
    import AppBar from "../components/AppBar.svelte";
    import Footer from "../components/footer.svelte";
    import { page } from '$app/stores';
    export let showNameBar; 
    export let name;

</script>
<header>
    <AppBar showNameBar="{
        //if its the home page, show the name bar
        $page.path === '/'
    }" bind:search={name} />
</header>

<slot />

<footer>
    <Footer />
</footer>