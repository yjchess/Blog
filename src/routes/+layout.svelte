<script>
    import Header from "../lib/header.svelte";
    import "../global.css"
  import Nav from "../lib/nav.svelte";
  import Foooter from "../lib/foooter.svelte";
</script>

<Header/>
<Nav/>

<main>
    <slot/>
</main>

<Foooter/>

<style>
    /* main{
        flex-grow: 1;
        width: 100%;
        background: rgb(30,30,30);
        -webkit-box-shadow: inset 0 0 40px 0px dimgrey;
        box-shadow: inset 0 0 40px 20px black;
        justify-content: space-between;
        align-items: center;
        box-sizing: border-box;
        border: 5px solid black;
    } */
</style>
