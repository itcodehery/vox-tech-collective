<script>
    import AppBar from "../../components/AppBar.svelte";
    const aboutScript = "We are a student-driven community of people passionate about the ever-evolving landscape of technology. This is more than just a Discord Server. We came up with the idea to help create a comfortable space to discuss, debate, learn and collaborate on technology and related topics.";
    const hobbyScript = "Networking is a huge part of what drives tech related hobbies and jobs. I believe a common platform where people can share ideas, contribute on Projects and collaborate together is essential in providing opportunities to build personal networks and I think that's what we've set out to do.";
    const structureScript = "Since the collective is community-driven, there is no thing as a leader or a manager. We hold discussions and meetings on things that we could do within the community. Currently we have something called Skill evaluation events going on where we do individual projects and showcase them to each other. Soon, we're planning on starting small scale projects that our community members would form teams and complete.";
    const futureScript = "We're looking to expand our community to other colleges and universities in Bangalore and eventually to other cities in India. We're also looking to collaborate with other tech communities and organizations to host events and workshops. In the future, we might move into freelancing and internships for our community members. We're looking for moderators and community managers to help us with the expansion. If you are interested in that, you can apply via the form link below.";

    function joinUsClick() {
        window.open('https://tally.so/r/meeq4e', '_blank');
    }
</script>

<style>
    @import '../../font-import.css';

    body {
        background-color: #0d1003;
        color:#d4e4a7;
    }
    .section-gap {
        height: 40px;
    }

    section {
        display: flex;
        flex-direction: column;
        align-items: left;
        justify-content: center;
        padding: 20px 280px;
    }

    h1 {
        color: #9cc032;
    }

    button {
        background-color: #B3E02B;
        color: #273d0b;
        padding: 8px 16px;
        border: none;
        border-radius: 6px;
        font-size: small;
        font-family: 'Raleway';
        font-weight: bold;
        cursor: pointer;
        font-weight: bold;
    }

    button:hover {
        background-color: #87AA1D;
    }
</style>

<header>
    <AppBar showNameBar="{false}"/>
</header>

<body>
    <div style="height: 60px;"/>
    <section>
        <h1>About Us</h1>
        <p>{aboutScript}</p>
        <h1>For Hobbies and Ambitions</h1>
        <p>{hobbyScript}</p>
        <h1>What exactly do we do?</h1>
        <p>{structureScript}</p>
        <h1>What's the future?</h1>
        <p>{futureScript}</p>
        <div class="section-gap"/>
        <button on:click={joinUsClick}>Moderation Application Form</button>
    </section>
</body>

