<script>
    let hue = 0

    setInterval(() => {
        hue ++
    }, 100);
</script>
<main>
    <div class="container" >
        <img class="image" src="/ethan.png">
        <div class="child" style="background-color:hsl({hue}, 100%, 50%)">
            <button onclick="document.location='week1'">Week 1</button>
            <button>Week 2</button>
            <button>Week 3</button>
            <button>Week 4</button>
        </div>
    </div>
</main>



<style>
    main {
        background: url("/snowie.png");
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
    .container {
        width: 600px;
        /* Center vertically and horizontally */
        position: absolute;
        top: 50%;
        left: 50%;
        margin: -300px 0 0 -300px;
    }
    .child {
        background-color: white;
        margin: 5px;
        padding: 0;
        position: relative;
        display: flex;

    }
    button {
        margin-bottom: 5px;
        margin-top: 5px;
        width: 190px;
        padding-bottom: 10px;
        padding-top: 10px;
        cursor: pointer;
        background-color: snow;
    }
    .image {
        width: 100%;
    }
</style>