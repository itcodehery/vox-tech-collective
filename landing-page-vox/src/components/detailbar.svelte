<script>
    import { IconUser } from "@tabler/icons-svelte";
    export let title;
    export let subtitle;
    export let buttonText;
    export let buttonAction;
</script>

<div class="bar">
    <div class="icon">
        <IconUser color="#000" size="20" fill="black" />
    </div>
    <div class="content">
        <h3>{title}</h3>
        <p>{subtitle}</p>
    </div>
    <button on:click={buttonAction}>{buttonText}</button>
</div>

<style>
    .bar {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        padding: 10px;
        background-color: #00000011;
        border: 1px solid #00000011;
        border-radius: 10px;
        margin-top: 20px;
        margin-bottom: 20px;
    }

    .icon {
        display: grid;
        place-items: center;
        margin-right: 10px;
        padding: 4px;
        background-color: white;
        border-radius: 10px;
    }

    .content {
        flex-grow: 1;
    }

    h3 {
        margin: 0;
        font-size: 18px;
        font-family: "SFProDisplayBold", sans-serif;
    }

    p {
        margin: 0;
        font-size: 14px;
        color: rgba(0, 0, 0, 0.419);
    }

    button {
        padding: 8px 16px;
        background-color: #000000d7;
        font-family: "SFProDisplayBold", sans-serif;
        color: #fff;
        border: none;
        border-radius: 50px;
        cursor: pointer;
    }
</style>
