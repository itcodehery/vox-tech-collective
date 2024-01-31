<script>
import AppBar from "../../components/AppBar.svelte";
let name = "world";
export let contacts = [{
        image: "https://avatars.githubusercontent.com/u/129949346?v=4",
        name: "Hari",
        fullname: "Hari Prasad",
        email: "haririo321@gmail.com"
    },
    {
        image: "https://avatars.githubusercontent.com/u/84909648?v=4",
        name: "Vaibhav",
        fullname: "Vaibhav Kumaar Murugendra",
        email: "vaibhavmurugendra@gmail.com"
    }];

    let curators = [{
        image: "https://avatars.githubusercontent.com/u/129949346?v=4",
        name: "Tamanna",
        fullname: "Tamanna Billuraj",
        email: "tamannabilluraj1564@gmail.com"
    },
    {
        image: "https://avatars.githubusercontent.com/u/120126451?v=4",
        name: "Aditya",
        fullname: "Aditya Salgundi",
        email: "adityasalgundi7@gmail.com"
    }
    ]
</script>

<style>
@import '../../font-import.css';

body {
    padding: 20px;
}

body h1 {
    padding: 20px;
    align-items: center;
    text-align: center;
    align-content: center;
}

.container {
    background-color: transparent;
    color: #fff;
    align-self: center;
    justify-self: center;
    gap: 20px;
    padding: 40px;
    display: flex;
    align-items: center;
    align-self: center;
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

@media screen and (max-width: 600px) {
    .container {
        background-color: transparent;
        color: #fff;
        align-self: center;
        justify-self: center;
        gap: 20px;
        padding: 40px;
        display: flex;
        align-items: center;
        align-self: center;
        justify-content: center;
        flex-direction: column;
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
                <h2>{contact.name}</h2>
                <p style="font-style: italic; color:gray">{contact.fullname}</p>
                <a href="{contact.email}">{contact.email}</a>
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
                <img src={curator.image} alt="Avatar">
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