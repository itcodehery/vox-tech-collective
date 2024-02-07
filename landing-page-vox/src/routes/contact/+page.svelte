<script>
import AppBar from "../../components/AppBar.svelte";
export let contacts = [{
        image: "https://avatars.githubusercontent.com/u/129949346?v=4",
        name: "Hari",
        fullname: "Hari Prasad",
        email: "haririo321@gmail.com",
        link: "linktr.ee/itwritshery"
    },
    {
        image: "https://avatars.githubusercontent.com/u/84909648?v=4",
        name: "Vaibhav",
        fullname: "Vaibhav Kumaar Murugendra",
        email: "vaibhavmurugendra@gmail.com"
    }];

    let curators = [{
        name: "Tamanna",
        fullname: "Tamanna Billuraj",
        email: "tamannabilluraj1564@gmail.com"
    },
    {
        name: "Aditya",
        fullname: "Aditya Salgundi",
        email: "adityasalgundi7@gmail.com"
    }
    ];

    function linkClick(link) {
        window.open("https://" + link, "_blank");
    }
</script>

<style>
@import '../../font-import.css';

body {
    padding: 20px;
    background-color: #0d1003;
}

body h1 {
    padding: 20px;
    align-items: center;
    text-align: center;
    align-content: center;
}

section {
    padding: 40px;
    gap: 20px;
}

.container {
    background-color: transparent;
    color: #fff;
    align-self: center;
    justify-self: center;
    gap: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: row;
    flex-shrink: inherit;
    width: clamp(200px, 50%, 600px);
    border-radius: 8px;
}

.g {
    background-color: #ffffff13;
    color: white;
    padding: 4px 20px;
    display: block;
    border-radius: 8px;
    width: clamp(240px, 0%, 500px);
}
.sub-heading {
    color: #b8ff5a;
}
body img {
    width:240px; 
    padding-top: 14px; 
    align-self: center;
    justify-self: center; 
    border-radius: 8px;
}

body a {
    padding-bottom: 20vb;
    gap: 20px;
    color: #9dcd5f;
}

    .linktree {
        background-color: rgb(46, 60, 0);
        color: #B3E02B;
        font-weight: bold;
        letter-spacing: 2px;
        height: 22px;
        padding: 4px 14px;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        transition: background-color 0.3s ease-in;
    }

    .linktree:hover {
        background-color: rgb(22, 28, 0);
        color: #B3E02B;
        font-weight: bold;
        letter-spacing: 2px;
        min-height: 10px;
        height: 22px;
        padding: 4px 14px;
        border: none;
        border-radius: 4px;
    }

    .nameRow {
        display: flex;
        flex-direction: row;
        align-items: center;
        align-self: center;
        justify-content: space-between;
        margin: 0px;
    }
    
@media screen and (max-width: 600px) {
    .container {
        background-color: transparent;
        color: #fff;
        align-self: center;
        justify-self: center;
        gap: 20px;
        display: flex;
        align-items: center;
        text-align: center;
        align-self: center;
        justify-content: center;
        flex-direction: column;
        flex-shrink: inherit;
        width: clamp(200px, 50%, 600px);
        border-radius: 8px;
    }

    section {
        padding: 20px;
        gap: 20px;
    }

    .g {
        background-color: #ffffff13;
        color: white;
        padding: 4px 20px;
        display: block;
        border-radius: 8px;
        width: clamp(240px, 0%, 500px);
    }
    body img {
        width:240px; 
        padding-top: 14px; 
        align-self: center;
        justify-self: center; 
        border-radius: 8px;
    }

    body a {
        padding-bottom: 20vb;
        gap: 20px;
        color: #9dcd5f;
    }
}
</style>

<body>
    <AppBar formAppBar="{true}"/>
        <div style="height: 60px;">
        </div>
        <h1 style="font-size: 36px;">Contact Us</h1>
        <section>
            <h2 class="sub-heading">Founders</h2>
            <div class="container"> 
            {#each contacts as contact}
            <div class="g">
                <img src={contact.image} alt="Avatar">
                <div class="nameRow">
                    <h2>{contact.name}</h2>
                    {#if contact.link}
                    <div style="height=20;"/>
                    <button class="linktree" on:click={linkClick(contact.link)}>LINKTREE</button>
                    {/if}
                </div>
                <p style="font-style: italic; color:gray">{contact.fullname}</p>
                <a href="mailto:{contact.email}">{contact.email}</a>
                
                <p></p>
            </div>
            {/each}
        </div>
        <div style="height=10;"/>
        </section>
        <section>
            <h2 class="sub-heading">Curators</h2>
        <div class="container"> 
            {#each curators as curator}
            <div class="g">
                <!-- <img src="{}" alt="Avatar"> -->
                <h2>{curator.name}</h2>
                <p style="font-style: italic; color:gray">{curator.fullname}</p>
                <a href="mailto:{curator.email}">{curator.email}</a>
                <p></p>
            </div>
            {/each}
        </div>
        <div style="height=10;"/>
        </section>
</body>