<script>
    export let url;
    export let breed;
</script>

<div class="cat">
    <img src={url} alt={breed} />
    <p>{breed}</p>
</div>

<style>
    .cat {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .cat img {
        height: 200px;
        width: 200px;
        object-fit: cover;
    }
</style>
