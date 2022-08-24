<script>
    export let titolo;
    export let actionType;
    const ACTIONS = {
        'start': 'pannello-start',
        'stop': 'pannello-stop',
        'kill':'pannello-kill',
        'restart':'pannello-restart'
    }

    function makeRequest(mouseEvent) {
        fetch(`localhost:3000/${ACTIONS[actionType]}`, {
            method: 'POST',
            headers: {'Content-Type': 'application/json'},
            body: JSON.stringify(),
        })
        .then((response) => response.json())
        .then((data) => console.log("BOTTONE-MS: ",data.msg));
    }

</script>

<button class="bottonePannello" on:click="{makeRequest}">
    {titolo}
</button>

<style>
    button.bottonePannello {
        margin-left: 1%;
        margin-right: 1%;
        color: white;
        background-color: #597ca3;
    }
    button.bottonePannello:hover {
        transition: all 0.25s;
        background-color: aliceblue;
        color: black;
    }
</style>
