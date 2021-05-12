<script>
    export let images;
</script>

<div class="carousel">
    <div class="carousel__container">
        {#each images as image (image.id)}
            <img src={image.path} alt={image.alt} id={image.id} height="300" />
        {/each}
    </div>
</div>

<style>
    .carousel {
        display: flex;
        overflow-x: auto;
        position: relative;
        width: 300% auto;
    }
    .carousel__container {
        display: flex;
    }
</style>
