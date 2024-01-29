<script>
    export let number;
    export let text;
</script>
<style>
    .number-card {
        background-color: #242d09;
        color: #b8ff5a;
        align-self: center;
        padding: 80px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        grid-template-columns: repeat(2, 1fr);
        grid-gap: 16px;
        border-radius: 8px;
        flex-direction: row-reverse;
    }

    .number-card h1 {
        margin: 0;
        font-size: 32px;
    }

    .number-card p {
        word-wrap: break-word;
        max-width: 400px;
    }
</style>
<div class="number-card">
    <div>
        <h1>{number}</h1>
        <p>{text}</p>
    </div>
</div>