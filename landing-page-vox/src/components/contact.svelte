<script>
    import { IconUsers } from "@tabler/icons-svelte";
    let allContacts = {
        "Hari Prasad": {
            role: "Community Manager",
            site: "hariprasad-one.vercel.app",
        },
        "Vaibhav Kumaar": {
            role: "Community Manager",
            site: "www.vaibhavmurugendra.tech",
        },
    };

    function openNewSite(site) {
        window.open(`https://${site}`, "_blank");
    }

    let allCurators = {
        "Tamanna Billuraj": {
            role: "Curator",
            email: "tamannabilluraj@gmail.com",
        },
        "Prathik Vishnu S": {
            role: "Curator",
            email: "prathik.pvs03@gmail.com",
        },
        "Pranav S": {
            role: "Curator",
            email: "panu.5631@gmail.com",
        },
        "Krithik M": {
            role: "Curator",
            email: "krithikm923@gmail.com",
        },
    };
</script>

<div class="globalwrap">
    <div class="row">
        <h1>Community Managers</h1>
        <button class="contactbutt">Contact Us</button>
    </div>
    <div class="cards">
        {#each Object.entries(allContacts) as [name, contact]}
            <div class="card">
                <h4>{name}</h4>
                <div style="display: flex; flex-direction: row; gap: 10px;">
                    <IconUsers color="#000" size="20" fill="black" />
                    <p>{contact.role}</p>
                </div>
                <button on:click={() => openNewSite(contact.site)}
                    ><p>{contact.site}</p></button
                >
            </div>
        {/each}
    </div>
    <div class="row">
        <h1>Community Curators</h1>
        <button class="contactbutt">Contact Us</button>
    </div>
    <div class="cardgrid">
        {#each Object.entries(allCurators) as [name, contact]}
            <div class="card">
                <h4>{name}</h4>
                <div style="display: flex; flex-direction: row; gap: 10px;">
                    <IconUsers color="#000" size="20" fill="black" />
                    <p>{contact.role}</p>
                </div>
                <button
                    ><a href="mailto:{contact.email}"><p>{contact.email}</p></a
                    ></button
                >
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
    }

    .row {
        display: flex;
        flex-direction: row;
        align-items: center;
        width: 700px;
        justify-content: space-between;
        gap: 10px;
        margin-top: 10px;
        padding-top: 30px;
        padding-bottom: 10px;
    }

    .cards {
        display: flex;
        flex-direction: row;
        gap: 10px;
    }

    .cardgrid {
        display: grid;
        grid-template-columns: 1fr 1fr;
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
        border-radius: 24px;
        cursor: cell;
    }

    .card:hover {
        background-color: rgba(0, 0, 0, 0.027);
    }

    a {
        text-decoration: none;
        color: white;
        padding: 0;
        border-radius: 0px;
        margin: 0;
    }

    @media (max-width: 768px) {
        .card {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            width: 100%;
            margin-top: 10px;
            margin-left: 20px;
            margin-right: 20px;
        }

        .row {
            flex-direction: column;
        }

        .cards {
            flex-direction: column;
            place-items: center;
        }

        .cardgrid {
            grid-template-columns: 1fr;
            place-items: center;
        }

        h4 {
            font-size: 24px;
        }

        h1 {
            font-size: 30px;
        }

        .contactbutt {
            display: none;
        }
    }
</style>
