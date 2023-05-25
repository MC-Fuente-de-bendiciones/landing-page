<script>
    import conviccionesVideo from '$lib/videos/convicciones.mp4';
    import conviccionesPoster from '$lib/images/cmn/convicciones-poster.jpeg';
    import {fade, fly} from 'svelte/transition';

    export let videoFinalizado = false;

    const toggleMuted = (event) => {
        event.target.muted = !event.target.muted;
    };

    const onEnded = () => {
        videoFinalizado = true;
    };

    $: videoFinalizado;
</script>

<section id="hero" class="h-section flex justify-center items-center px-4">
    {#if !videoFinalizado}
        <div class="w-full h-fit absolute md:w-4/5 lg:w-1/2 xl:w-1/2 p-4">
            <video on:ended={onEnded}
                   on:click={toggleMuted}
                   in:fade={{duration: 1500}}
                   out:fly="{{y: 100, duration: 200}}"
                   autoplay
                   playsinline
                   poster="{conviccionesPoster}"
                   class="w-full rounded-2xl">
                <source src="{conviccionesVideo}"/>
            </video>
        </div>
    {:else}
        <div class="flex flex-col gap-8 w-limit text-center">
            <span in:fly="{{y: -50, duration: 500, delay: 500}}"
                  class="portrait:text-[5vh] landscape:text-[4vw] text-white font-dela-gothic-one uppercase">
                Congreso juvenil
            </span>
            <span in:fly="{{y: -50, duration: 500, delay: 1000}}"
                  class="portrait:text-[4vh] landscape:text-[4vw] text-yellow-300 font-dela-gothic-one uppercase">
                Convicciones 2.0
            </span>
            <picture in:fly="{{y: -50, duration: 500, delay: 1500}}" class="w-full lg:w-1/2 m-auto">
                <img src="{conviccionesPoster}" alt="conviccionesPostal" class="rounded-lg shadow-2xl w-full">
            </picture>
        </div>
    {/if}
</section>


<style lang="postcss">
    #hero {
        background: url('/src/lib/backgrounds/layered-waves-cmn.svg') no-repeat center center;
        background-size: cover;
    }

    .w-limit {
        @apply max-w-[100%] md:max-w-[90%] lg:max-w-[80%] xl:max-w-[70%];
    }
</style>