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
        margin-top: 30px;
    }

    .card-row {
        display: flex;
        flex-wrap: wrap;
    }

    h4 {
        margin: 0;
        color: rgb(36, 113, 237);
        font-size: small;
    }

    h1 {
        font-family: "SFProDisplayBold", sans-serif;
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
    }
</style>
