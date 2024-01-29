<script>
    export let mainText;
    export let subText;
    import header from '../lib/images/header.png'
</script>
<style>
    .tertiary-card {
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

    .tertiary-card h1 {
        margin: 0;
        font-size: 32px;
    }

    .tertiary-card p {
        word-wrap: break-word;
        max-width: 400px;
    }
</style>
<div class="tertiary-card">
    <div>
        <h1>{mainText}</h1>
        <p>{subText}</p>
    </div>
    <div>
        <img src="{header}" alt="logo" width="555px" height="222px"/>
    </div>
    
</div>