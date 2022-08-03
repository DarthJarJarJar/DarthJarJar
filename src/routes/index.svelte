<script>




    let opacity = -0
    let elem;
    function click() {
        opacity+=5
        elem.style.opacity=`${opacity}%`
    }
 
    
</script>
<body on:click={click}>
    <h1>
        Keep clicking anywhere on the page
    </h1>
    {#if (opacity>=20)}
    <!-- svelte-ignore a11y-missing-attribute -->
    <iframe id="ytplayer" type="text/html" width="640" height="360"
    src="https://www.youtube.com/embed/dQw4w9WgXcQ?autoplay=1" allow="autoplay"
    frameborder="0"></iframe>
    {:else}    <img id="rr" bind:this={elem} src="src/rickroll4k.jpeg" alt="rickroll">

    {/if}

</body>

<style>
    iframe {
        margin-left: auto;
        margin-right: auto;
        text-align: center;
        display: block;
    }
    img {
        opacity: 0%;
        position: absolute;
        top: 0;
    }
    h1 {
        text-align: center;
        font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    }
</style>