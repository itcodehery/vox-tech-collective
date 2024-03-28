<script>
    let expandedItem = null;

    function toggleItem(item) {
        expandedItem = expandedItem === item ? null : item;
    }

    const items = {
        "#1": {
            id: "#1",
            icon: "📚",
            title: "Have Discussions on Tech and its impact on the community",
            content:
                "We have discussions on various topics in tech and how it impacts the community. We discuss the latest trends and how we can contribute to the community.",
        },
        "#2": {
            id: "#2",
            icon: "🛠️",
            title: "Work on Projects together and build portfolios of each other",
            content:
                "We work on projects together and build portfolios of each other. We help each other grow and learn new skills.",
        },
        "#3": {
            id: "#3",
            icon: "🎉",
            title: "Have fun and learn together in a safe environment",
            content:
                "We have fun and learn together in a safe environment. We make sure that everyone is comfortable and has a good time.",
        },
    };
</script>

<div class="text">
    <p style="color: #838383; font-family: 'SFProDisplayRegular';">
        What are we hoping for
    </p>
    <h1>Aims</h1>
</div>
<div class="accordion">
    {#each Object.values(items) as yoooo}
        <div class="accordion-item">
            <button
                class="accordion-header"
                on:click={() => toggleItem(yoooo.id)}
            >
                <div class="titleheader">
                    <p>{yoooo.icon}</p>
                    <p>{yoooo.title}</p>
                    {expandedItem === yoooo.id ? "▲" : "▼"}
                </div>

                <div
                    class="accordion-content"
                    style={expandedItem === yoooo.id ? "" : "display: none;"}
                >
                    {yoooo.content}
                </div>
            </button>
        </div>
    {/each}
</div>

<style>
    .accordion {
        display: flex;
        flex-direction: column;
        align-self: center;
        align-items: center;
        justify-content: center;
        gap: 10px;
        width: 100%;
        max-width: 500px;
        color: black;
    }

    .accordion-item {
        display: flex;
        flex-direction: row;
        font-family: "SFProDisplayRegular", sans-serif;
        background-color: #ffffff28;
        border: 1px solid #ccc;
        border-radius: 8px;
        width: 100%;
    }

    .accordion-header {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        padding: 10px;
        font-family: "SFProDisplayBold", sans-serif;
        background-color: #f5f5f5;
        border-bottom: 1px solid #ccc;
        border-radius: 8px 8px 0 0;
        cursor: pointer;
        transition: ease-in-out 0.2s;
        width: 100%;
    }

    .titleheader {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        width: 100%;
    }

    .accordion button {
        background: none;
        border: none;
        cursor: pointer;
    }

    .accordion-content {
        border-top: 1px solid #fff;
        padding: 4px;
        margin-top: 10px;
        border: dashed 1px #a8a8a8;
        border-radius: 0 0 8px 8px;
        transition: ease-in-out 0.2s;
        text-align: left;
        font-family: "SFProDisplayRegular", sans-serif;
    }

    @media (max-width: 768px) {
        .accordion {
            width: 95%;
            max-width: 100%;
        }
    }
</style>
