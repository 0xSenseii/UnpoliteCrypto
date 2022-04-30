<script>
    export let connected;
    export let account;

    connected = false;
    account = null;

    const connect = async () => {
        if (window.ethereum) {
            await window.ethereum.send("eth_requestAccounts");
            window.web3 = new Web3(window.ethereum);
            var accounts = await web3.eth.getAccounts();
            account = accounts[0];
            connected = true;
        }
    };
</script>

<div class="container">
    <button class="button-50" id="connectButton" on:click={connect}
        >Connect to Metamask</button
    >
</div>

<style>
    /* center content from container class */
    .container {
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
    }

    .button-50 {
        appearance: button;
        background-color: #000;
        background-image: none;
        border: 1px solid #000;
        border-radius: 4px;
        box-shadow: #fff 4px 4px 0 0, #000 4px 4px 0 1px;
        box-sizing: border-box;
        color: #fff;
        cursor: pointer;
        display: inline-block;
        font-size: 14px;
        font-weight: 400;
        line-height: 20px;
        margin: 0 5px 10px 0;
        overflow: visible;
        padding: 12px 40px;
        text-align: center;
        text-transform: none;
        touch-action: manipulation;
        user-select: none;
        -webkit-user-select: none;
        white-space: nowrap;
    }

    .button-50:focus {
        text-decoration: none;
    }

    .button-50:hover {
        text-decoration: none;
    }

    .button-50:active {
        box-shadow: rgba(0, 0, 0, 0.125) 0 3px 5px inset;
        outline: 0;
    }

    .button-50:not([disabled]):active {
        box-shadow: #fff 2px 2px 0 0, #000 2px 2px 0 1px;
        transform: translate(2px, 2px);
    }

    @media (min-width: 768px) {
        .button-50 {
            padding: 12px 50px;
        }
    }
</style>
