<script>
import AppBar from "../../components/AppBar.svelte";
import Footer from "../../components/footer.svelte";
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
 let members = [{
        image: "https://avatars.githubusercontent.com/u/120126451?v=4",
        name: "Aditya",
        fullname: "Aditya Salgundi",
        email: "adityasalgundi@gmail.com"
}, 
    {
        image: "https://avatars.githubusercontent.com/u/84909648?v=4",
        name: "Kevin",
        fullname: "Kevin S",
        email: "kevins@gmail.com"
    }
];
</script>

<style>
@import '../../font-import.css';

hr {
    width: 30%;
    color: rgba(255, 255, 255, 0.111);
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
    flex-direction: row;
    flex-shrink: inherit;
    width: clamp(200px, 50%, 600px);
    border-radius: 8px;
}

.g {
    background-color: #fff;
    color: black;
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
}
</style>

<body>
    <AppBar bind:search="{name}"/>
        <div style="height: 65px;">

        </div>
        <h1 style="font-size: 36px;">Contact Us</h1>
        <hr/>
        <h1 class="sub-heading">Founders</h1>
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
        <hr/>
        <h1 class="sub-heading">Curators</h1>
        <div class="container"> 
            <div class="g">
                <img src="https://avatars.githubusercontent.com/u/129949346?v=4" alt="Avatar">
                <h2>Tamanna</h2>
                <p style="font-style: italic; color:gray">Tamanna Billuraj</p>
                <a href="mailto:tamannabilluraj@gmail.com">tamannabilluraj@gmail.com</a>
                <p></p>
            </div>
        </div>
        <hr/>
        <h1 class="sub-heading">Members</h1>
        <div class="container"> 
            {#each members as member}
            <div class="g">
                <img src={member.image} alt="Avatar">
                <h2>{member.name}</h2>
                <p style="font-style: italic; color:gray">{member.fullname}</p>
                <a href="mailto:{member.email}">{member.email}</a>
                <p></p>
            </div>
            {/each}
        </div>
            </body>
            <footer>
                <Footer/>
            </footer>
