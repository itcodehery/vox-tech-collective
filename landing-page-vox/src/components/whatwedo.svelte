<script>
    export let categoryTitle;
    export let title;

    let items = {
        "#1": "Have Discussions on Tech and its impact on the community",
        "#2": "Work on Projects together and build portfolios of each other",
        "#3": "Have fun and learn together in a safe environment",
    };
</script>

<div class="whatwedo">
    <h4>{categoryTitle}</h4>
    <h1>{title}</h1>

    <div class="card-row">
        {#each Object.entries(items) as [key, value]}
            <div class="card">
                <h4>{key}</h4>
                <p>{value}</p>
            </div>
        {/each}
    </div>
</div>

<style>
    .whatwedo {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        font-family: "SFProDisplayRegular", sans-serif;
        margin-top: 30px;
    }

    .card-row {
        display: flex;
        flex-wrap: wrap;
    }

    h4 {
        margin: 0;
        color: #838383;
        font-size: small;
    }

    h1 {
        font-family: "YoungSerif", sans-serif;
        font-size: 40px;
        margin: 10px;
        max-width: 500px;
        text-align: center;
        letter-spacing: -0.5px;
    }

    .card {
        width: 200px;
        padding: 16px;
        margin: 8px;
        border: 1px solid #ccc;
        border-radius: 8px;
        cursor: cell;
    }

    .card:hover {
        background-color: rgba(0, 0, 0, 0.027);
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

        h4 {
            font-size: 24px;
        }
    }
</style>
