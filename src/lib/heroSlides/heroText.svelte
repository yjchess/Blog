<script>
    export let textSlide = 0;
</script>

<form action="">
    <fieldset>

{#if textSlide === 0}
    <legend><h2>Rapidfire FAQ</h2></legend>
    <div class="flex">

        <p>Kinds of posts to expect in Technology:</p>
        <ol>
            <li>Project plans, execution, reflection / analysis...</li>
            <li>Cheatsheets, guides, explanations...</li>
            <li>Discussions, analysis...</li>
        </ol>

        
        <p>Kinds of posts to expect in Hobby:</p>
        <ol>
            <li>Electronics</li>
            <li>Writing</li>
            <li>Art, Reading, 3D Modelling, Other</li>
        </ol>

        <p>Kinds of posts to expect in Miscellaneous:</p>
        <ol>
            <li>Personal Philosophy</li>
            <li>Mental Health & Reflection</li>
            <li>Plans for the future, progress reports & diary.</li>
        </ol>
    </div>
{:else if textSlide ===1}
    <legend><h2>Examples</h2></legend>
    <div class="flex">
        <p>Technology:</p>
        <ol>
            <li>Blog post about the making of this blog.</li>
            <li>Blog post on common sveltekit mishaps.</li>
            <li>Blog post on how to approach a project.</li>
        </ol>
        
        <p>Hobby:</p>
        <ol>
            <li>Blog post on Soldering: tips and tricks.</li>
            <li>Blog post about "Anxious Hero" novel.</li>
            <li>Blog post about my hobby aims & goals.</li>
        </ol>
        
        <p>Miscellaneous:</p>
        <ol>
            <li>Blog post on the Dunning Kruger effect.</li>
            <li>Blog post on trying to balance work & fun.</li>
            <li>Blog post on my two year plan 2023-2025.</li>
        </ol>
    </div>


{:else if textSlide ===2}
    <legend><h2>About</h2></legend>
    <div class="flex paragraph-spacing">
        <p> Hello everyone, this blog is partially a selfish endeavour in that I will be using it to keep track of my progress and to motivate myself, however - that being said, I will also be seeking to help others with this blog.</p>
        <p>This blog seeks to provide you all with the perspective of someone self-teaching himself programming. It will be an unfiltered view of the entire journey leaving out no detail. It will be an honest view of how someone who has struggled in the past with mental health issues carves his way into a brighter future. I hope that others may be able to follow in my footsteps.</p>
        <p>Additionally, I will be creating resources such as guides, cheatsheets, summaries etc. and for each blogpost I may create multiple versions to show: A barebones version, a lengthy version and a slightly more chaotic version with my thoughts and feelings. You can read more about this blog <button>Here</button></p>    
    </div>

{:else if textSlide ===3}
    <legend><h2>Showcase</h2></legend>
    <div class="flex">
        <p>Here is a showcase of some of the projects made (and discussed within my blogs):</p>
        <div class="project1">
            <p>[Title of Project 1]</p>
            <p>[Image for Project 1]</p>
            <p>[Github Link for Project 1]</p>
            <p>[Blog Link for Project 1]</p>
        </div>
    
        <div class="project2">
            <p>[Title of Project 2]</p>
            <p>[Image for Project 2]</p>
            <p>[Github Link for Project 2]</p>
            <p>[Blog Link for Project 2]</p>
        </div>
    </div>



{/if}

    </fieldset>
</form>

<style>

    h2{
        margin:0;
    }

    form, fieldset{
        margin:0;
        padding-bottom:0;;
        padding-top: 0;
        box-sizing: border-box;
    }

    form{
        min-height:350px;
    }

    fieldset{
        min-height:350px;
        display: flex;
    }

    .flex{
        display: flex;
        flex-grow: 1;
        min-height: 320px;
        height: 100%;
        flex-direction: column;
        justify-content:space-evenly;
    }


    p{
        margin: 0;
        /* padding: 10px 0px; */
    }

    /* Need this for mobile view */
    .paragraph-spacing p{
        padding: 5px 0px;
    }

    ol{
        margin: 0;
    }

    button{
        margin:0;
        padding:0 10px;
        background-color: black;
        color: cyan;
        font-weight: bolder;
        line-height: 15px;
    }






</style>