<script>
    import avatar from "$lib/assets/avatar.jpg"
    import HeroText from "./heroSlides/heroText.svelte";

    let textSlide=0;
    function changeTextSlide(change){
        if(textSlide === 3 && change === 1){textSlide=0; return}
        if(textSlide === 0 && change === -1){textSlide=3; return}
        textSlide += change;
    }
</script>

<div class="heroContainer">
    <div class="hero">
        <img src={avatar} alt="">
        <div class="heroText">
    
            <HeroText {textSlide}/>

            <div class="buttons">
                <button on:click={()=>changeTextSlide(-1)}>Previous</button>
                <button on:click={()=>changeTextSlide(1)}>Next</button>
            </div>
        </div>
    
    </div>

    <button class="heroButton">
       📰 Sign up to the Newsletter now! 📰
    </button>
</div>




<style>

    .heroContainer{
        width: fit-content;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-left: auto;
        margin-right: auto;
        padding-left:25px;
        padding-right: 25px;
    }

    .hero{
        padding: min(5vw,55px);
        margin-top: 25px;
        margin-bottom: 25px;
        background-color: darkgreen;
        background: #0f0c29;  /* fallback for old browsers */
        background: -webkit-linear-gradient(to right, #24243e, #302b63, #0f0c29);  /* Chrome 10-25, Safari 5.1-6 */
        background: linear-gradient(to right, #24243e, #302b63, #0f0c29); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

        border-radius: 5vw;
        display: flex;
        justify-content: space-between;
        max-width: 1000px;
        box-sizing: border-box;

        border: 10px solid black;
    }

    img{
        width: 40%;
        height: 40%;
        border-radius: 20px;
        border: 5px solid black;
        box-sizing: border-box;
        margin-top:5px;
        margin-bottom:5px;
    }

    .heroText{
        width: 50%;
    }

    .buttons{
        display: flex;
        justify-content: space-between;
        padding: 10px;
    }

    .buttons button{
        width: 30%;
        min-width:70px;
        border-radius: 50px;
        font-weight: bolder;
        background-color: black;
        color:white;
    }

    button.heroButton{
        border-width: 5px;
        font-size: 25px;
        line-height: 30px;
        font-weight: bolder;
        height: 100px;
        width: 100%;
        background: #0f0c29;  /* fallback for old browsers */
        background: -webkit-linear-gradient(to right, #24243e, #302b63, #0f0c29);  /* Chrome 10-25, Safari 5.1-6 */
        background: linear-gradient(to right, #302b63, #24243e, #302b63); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
        border-radius: 10px;
        color: cyan;
        margin-bottom: 25px;
    }

    button.heroButton:active{
        padding-top: 10px;
    }

    button.heroButton:hover{
        cursor: pointer;
    }

    @media (max-width:1100px){
        .hero{
            flex-direction: column;
            /* padding-left: 10px;
            padding-right: 10px; */
            width:min(490px, 100%);
        }

       .heroText{
            width: fit-content;
            margin-top: min(5vw,55px);
        }

        img{
            width: 50%;
            align-self: center;
        }

        button.heroButton{
            width:min(490px, 100%);
        }


    }
</style>