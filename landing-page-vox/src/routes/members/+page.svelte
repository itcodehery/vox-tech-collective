<script>
    import AppBar from "../../components/AppBar.svelte";
    import Footer from "../../components/footer.svelte";
    import NumberCard from "../../components/numberCard.svelte";
    let memberCount = 0;
    let text = "members currently working on projects"

    let name = "world";
</script>
<style>
    @import '../../font-import.css';
    hr {
        width: 30%;
        color: rgba(255, 255, 255, 0.111);
    }  
</style>
<body>

    <AppBar bind:search={name}/>
    <div style="height: 50px;">
    </div>
    <hr/>
    <NumberCard bind:number="{memberCount}" bind:text="{text}"/>
</body>
<footer>
    <Footer/>
</footer>