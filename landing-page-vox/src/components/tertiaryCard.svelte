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

    @media screen and (max-width: 600px) {
        .tertiary-card {
            padding: 32px;
            flex-direction: column;
        }
        
        .tertiary-card h1 {
            font-size: 24px;
        }

        .tertiary-card .image {
            display: none;
            opacity: 0;
        }
    }

    .tertiary-card p {
        word-wrap: break-word;
        max-width: 400px;
        color: rgb(206, 227, 143);
    }

    .tertiary-card .image {
        /* make the image resize by width */
        width: min-content;
        height: min-content;
    }
</style>
<div class="tertiary-card">
    <div>
        <h1>{mainText}</h1>
        <p>{subText}</p>
    </div>
    <div class="image">
        <img src="{header}" alt="logo" width="555px" height="222px"/>
    </div>
</div>