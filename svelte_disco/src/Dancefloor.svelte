<script>
    import Lamp from "./Lamp.svelte";
    export let h;
    export let w;
    export let lampCount;

    let lamps = [];

    for (let i = 0; i < lampCount; i++) {
        lamps.push({
            lft: Math.random() * w,
            tp: Math.random() * h,
        });
    }

</script>

<div class="dancefloor" style="width: {w}px; height: {h}px;">
    {#each lamps as lamp}
        <Lamp links={lamp.lft} oben={lamp.tp} />
    {/each}
</div>

<style>
    .dancefloor {
        position: relative;
        background-color: #222;
        border: 4px solid gray;
        border-radius: 10px;
        padding:10px;
    }
</style>
