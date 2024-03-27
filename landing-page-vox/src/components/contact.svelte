<script>
    let allContacts = {
        "Hari Prasad": {
            role: "Community Manager",
            email: "haririo321@gmail.com",
        },
        "Vaibhav Kumaar": {
            role: "Community Manager",
            email: "vaibhavmurugendra@gmail.com",
        },
    };
</script>

<div class="globalwrap">
    <div class="row">
        <h1>Contact</h1>
        <button>Our Mail</button>
    </div>
    <div class="cards">
        {#each Object.entries(allContacts) as [name, contact]}
            <div class="card">
                <h4>{name}</h4>
                <p>{contact.role}</p>
                <a href="mailto:{contact.email}"><p>{contact.email}</p></a>
            </div>
        {/each}
    </div>
</div>

<style>
    @import "../font-import.css";

    .globalwrap {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        font-family: "SFProDisplayRegular", sans-serif;
        margin-top: 30px;
        padding: 30px;
    }

    .row {
        display: flex;
        flex-direction: row;
        align-items: center;
        width: 700px;
        justify-content: space-between;
        gap: 10px;
        margin-top: 10px;
    }

    .cards {
        display: flex;
        flex-wrap: wrap;
    }

    button {
        background-color: rgb(0, 0, 0);
        color: white;
        font-family: "SFProDisplayRegular", sans-serif;
        border: 1px solid #fff;
        border-radius: 20px;
        padding: 8px 16px;
        cursor: pointer;
        margin-right: 10px;
        transition: ease-in-out 0.2s;
    }

    button:hover {
        background-color: rgb(0, 0, 0, 0.8);
    }

    button:active {
        scale: 0.95;
    }

    h1 {
        font-family: "YoungSerif", sans-serif;
        font-size: 40px;
        margin: 10px;
        max-width: 500px;
        text-align: center;
        letter-spacing: -0.5px;
    }
    h4 {
        font-size: large;
        margin: 0;
    }

    p {
        margin: 0;
    }

    .card {
        display: flex;
        flex-direction: column;
        gap: 10px;
        width: 300px;
        padding: 16px;
        margin: 8px;
        border: 1px solid #ccc;
        border-radius: 8px;
        cursor: cell;
    }

    .card:hover {
        background-color: rgba(0, 0, 0, 0.027);
    }

    a {
        text-decoration: none;
        color: black;
        padding: 4px;
        border-radius: 4px;
    }
</style>
