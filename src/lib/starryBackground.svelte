<script>
    import stars from "$lib/assets/stars/stars.png";
    import twinkling from "$lib/assets/stars/twinkling.png";
</script>

<div class="stars" style="background: #000 url({stars}) repeat top center"></div>
<div class="twinkling" style="background: transparent url({twinkling}) repeat top center"></div>
<div class="content">
    <slot/>
</div>


<style>

    @keyframes move-clouds-back{
        from {background-position: 0 0;}
        to {background-position: 10000px 0;}
    }

    @keyframes move-twinkle-back{
        from {background-position: 0 0;}
        to {background-position: -10000px 0;}
    }

    .stars, .twinkling{
        position: absolute;
        top:0;
        left:0;
        right:0;
        bottom:0;
        width: 100%;
        height: 100%;
        display: block;
    }

    .stars{
        z-index: 0;
    }

    .twinkling{
        z-index: 1;
        animation: move-twinkle-back 200s linear infinite;
    }

    .content{
        position: relative;
        z-index:3;
        background-color: transparent;
    }

</style>