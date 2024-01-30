<script>
    export let mainText;
    export let subText;
    import logo from '../lib/images/logo.png';
</script>
<style>
    .secondary-card {
        background-color: #242d09;
        background-image: url('../lib/images/secondaryCardbg.png');
        background-size: cover;
        color: #b8ff5a;
        align-self: center;
        padding: 80px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        grid-template-columns: repeat(2, 1fr);
        grid-gap: 16px;
        border-radius: 8px;
    }

    .secondary-card h1 {
        margin: 0;
        font-size: 32px;
    }

    @media screen and (max-width: 600px) {
        .secondary-card {
            padding: 32px;
            flex-direction: column;
        }
        
        .secondary-card h1 {
            font-size: 24px;
        }
    }

    .secondary-card p {
        word-wrap: break-word;
        max-width: 400px;
        font-kerning: normal;
        color: rgb(206, 227, 143);
    }
</style>
<div class="secondary-card">
    <div>
        <h1>{mainText}</h1>
        <p>{subText}</p>
    </div>
    <div>
        <img src={logo} alt="logo" width="140px" height="140px"/>
    </div>
</div>