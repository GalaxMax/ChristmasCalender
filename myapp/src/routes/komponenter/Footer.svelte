<script>

</script>
    <div class="footer" on:click={() => document.location='/'}>
        <h1>Back to UI</h1>
    </div>

<style>
    .footer {
        position:absolute;
        height: 7%;
        width: 10%;
        border-radius: 0 25px 0 0;
        left: 0;
        bottom:0;
        z-index: 1001;
        background: coral;
        color: white;
        padding-left: 16px;
        overflow: hidden;
    }
    .footer:hover {
        background: orangered;
        cursor: pointer;
    }
</style>