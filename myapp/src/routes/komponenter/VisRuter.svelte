<script>
    import {uke1Luker as luke} from "../JS/24Luker.js";
    export let index
    //alert('No peeking!')
    function getRandomInt(max) {
        return Math.floor(Math.random() * max);
    }
    let date = new Date()

    function checkForPeekers() {
        if (date.getDate() >= index+1){
            luke[index].snudd = true
        }
        else alert('No peeking!')
    }

</script>

    {#if luke[index].advent === false}
        <div class="rute" style="order: {getRandomInt(20)}" on:click={() => (checkForPeekers())}>
            {#if luke[index].snudd === true}
                <div class="opnet">{luke[index].quote}</div>
                {:else}
                <div class="bakside">{luke[index].nr}</div>
            {/if}
        </div>
        {:else}
        <div class="adventRute" style="order: {getRandomInt(20)}" on:click={() => (checkForPeekers())}>
            {#if luke[index].snudd === true}
                <div class="opnet">{luke[index].quote}</div>
            {:else}
                <div class="bakside">{luke[index].nr}</div>
            {/if}
        </div>
    {/if}

<style>
    .rute {
        width: 30%;
        height: 175px;
        margin-right: 40px;
        margin-top: 30px;
        margin-left: 20px;
        border: coral solid;
        flex-grow: 1;
        cursor: help;
    }
    .bakside {
        font-size: 60px;
        padding: 6px;
        color: white;
        text-align: center;
    }
    .opnet {
        background-color: white;
        height: 100%;
        font-size: 32px;
    }
    .adventRute {
        width: 340px;
        height: 275px;
        margin-right: 40px;
        margin-top: 30px;
        margin-left: 20px;
        border: darkorchid solid;
        flex-grow: 1.5;
    }
</style>