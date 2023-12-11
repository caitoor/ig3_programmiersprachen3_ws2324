<script>
    export let links;
    export let oben;

    let interval = Math.random() * 1000 + 100;

    let col = `rgb(${Math.random() * 255},${Math.random() * 255},${
        Math.random() * 255
    })`;

    let isShining = true;

    function toggleLamp() {
        isShining = !isShining;
    }

    setInterval(toggleLamp, interval);
</script>

<div
    class="lamp"
    class:hidden={!isShining}
    style="background-color: {col}; left: {links}px; top: {oben}px;"
></div>

<style>
    .lamp {
        position: absolute;
        height: 10px;
        width: 10px;
        border-radius: 50%;
        box-shadow: 0 0 5px white;
    }

    .hidden {
        opacity: 0;
        transition: opacity 0.3s ease-in-out;
    }
</style>
