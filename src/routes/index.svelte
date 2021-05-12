<script>
    import Carousel from '../components/Carousel.svelte';
    const images = [
        {
            path: 'https://img.blogs.es/anexom/wp-content/uploads/2016/08/hoteles-w-920x515.jpg',
            id: 'imagen-ejemplo-1',
            alt: 'Atributo ALT de ejemplo para la imagen #1',
        },
        {
            path: 'https://alfagemeviajes.com/images/uploads/Hotel.jpg',
            id: 'imagen-ejemplo-2',
            alt: 'Atributo ALT de ejemplo para la imagen #2',
        },
        {
            path: 'https://www.efetur.com/core/blogs.dir/2/files/2014/12/RP-Marrakech-Spa-low.jpg',
            id: 'imagen-ejemplo-3',
            alt: 'Atributo ALT de ejemplo para la imagen #3',
        },
        {
            path: 'https://www.i-decoracion.com/Uploads/i-decoracion.com/Imagenes/hotel-submarino-5-estrellas-poseidon-undersea.jpg',
            id: 'imagen-ejemplo-4',
            alt: 'Atributo ALT de ejemplo para la imagen #4',
        },
        {
            path: 'https://images.homify.com/c_fill,f_auto,h_500,q_auto,w_1280/v1437703120/p/photo/image/106238/ba_era-Teuco-Seaside__Tono_Bagno__Ba_os_Hotel_Mandarin__barcelona-suite-penthouse-bathroom-1.jpg',
            id: 'imagen-ejemplo-5',
            alt: 'Atributo ALT de ejemplo para la imagen #5',
        },
        {
            path: 'https://www.restauranthotelbar.com/fotos/4/Fairplay1.jpg',
            id: 'imagen-ejemplo-6',
            alt: 'Atributo ALT de ejemplo para la imagen #6',
        },
        {
            path: 'data:image/jpeg;base64,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',
            id: 'imagen-ejemplo-7',
            alt: 'Atributo ALT de ejemplo para la imagen #7',
        },
    ];
</script>

<main>
    
    <h2 class="item__title" align="center">Winter Hotel</h2>
    <div class="item__gallery">
        <Carousel {images} />
    </div>
    <p class="item__description" align="center">
        El hotel de Luffy
    </p>
</main>

<style>
    main {
        padding: 1em;
        max-width: 900px;
        margin: 0 auto;
    }
</style>

