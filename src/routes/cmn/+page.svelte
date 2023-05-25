<script>
    import conviccionesVideo from '$lib/videos/convicciones.mp4';
    import conviccionesPoster from '$lib/images/cmn/convicciones-poster.jpeg';

    const showPoster = (event) => {
        event.target.autoplay = false;
        event.target.load();
    };

</script>

<section id="hero" class="h-section flex justify-center py-12 px-4">
    <video
            on:ended={showPoster}
            poster="{conviccionesPoster}"
            autoplay
            muted
            playsinline
            controls="controls"
            class="w-full h-fit md:w-4/5 xl:w-1/2">
        <source src="{conviccionesVideo}"/>
    </video>
</section>


<style lang="postcss">
    #hero {
        background: url('/src/lib/backgrounds/layered-waves-cmn.svg') no-repeat center center;
        background-size: cover;
    }
</style>