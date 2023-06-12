<script>
  import Hero from "../lib/hero.svelte";
  import StarryBackground from "../lib/starryBackground.svelte";
</script>

<div class="heroBackground">
    
    <StarryBackground>
        <Hero/>
    </StarryBackground>

</div>

<div class="test">

</div>


<style>
    .heroBackground{
        position: relative;
    }

</style>