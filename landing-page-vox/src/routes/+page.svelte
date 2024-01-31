<script>
    import AppBar from "../components/AppBar.svelte";
    import MainCard from "../components/mainCard.svelte";
    import SecondaryCard from "../components/secondaryCard.svelte";
    import TertiaryCard from "../components/tertiaryCard.svelte";
    let name = "World";
</script>

<style>
@import '../font-import.css';
</style>

<header>
    <AppBar showNameBar="{true}" bind:search={name}/>
</header>

<body>
    <div style="height: 60px;">
    </div>
    <section>
        <div class="section-gap"/>
    <MainCard
        mainText="👋 Hello {name}! We are the Vox Technologia Collective"
        subText="A coder community of college students based in Bangalore, India!"/>
        <div class="section-gap"/>
    </section>
    <section>
        <div style="flex-direction: row;">
            <SecondaryCard
                imagePath = "/images/logo-opac.png"
                mainText = "What is this? 🤔"
                subText = "Hey, we are Hari and Vaibhav, the founders of the tech Collective.
                We would like to provide an opportunity to students who are interested
                in joining a Coding and Tech community of college students around
                Bangalore, India. We're looking for new people and recruits to join us."/>
        </div>
    </section>
    <section>
        <div class="section-gap"/>
        <TertiaryCard imagePath = "/images/logo-opac.png"
            mainText = "This is for you 🫵 if:"
            subText = "You are very passionate about technology, designing, 
            marketing or coding, or you are currently doing a degree or course 
            that is tech-related or incorporates tech, designing or coding in 
            any way and you're open minded about meeting new people and forming 
            collaborative groups with them. "/>
        <div class="section-gap"/>
    </section>
</body>
