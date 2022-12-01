<script>
    import VisRuter from "../komponenter/VisRuter.svelte";
    import {uke1Luker} from "../JS/24Luker.js";
    import Footer from "../komponenter/Footer.svelte";
</script>


<main>
    <div class="picture">
        {#each uke1Luker as luke, index}
            <VisRuter index={index}></VisRuter>
        {/each}
    </div>
</main>
<Footer></Footer>
<style>
    main {
        background: url("/week1.png");
        position:fixed;
        width:100%;
        height:100%;
        top:0;
        left:0;
        z-index:1000;
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
    }
    .picture {
        width: 100%;
        position: relative;
        display:flex;
        flex-flow:row wrap;
        font-size: 16px;
    }
</style>