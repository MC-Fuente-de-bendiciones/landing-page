<script>
    import bgVideoFdb from '$lib/videos/bg-video-fdb.mp4';
    import descImg from '$lib/images/photos/desc-img.png';
    import {Constants} from "../shared/constants/Constants.ts";

    const scrollIntoSection = () => {
        const sectionAbout = document.getElementById('section-about');
        scrollY = sectionAbout.offsetTop - Constants.navbarHeight;
        scroll({
            top: scrollY,
            behavior: 'smooth'
        });
    };
</script>

<section class="h-section flex">
    <video autoplay
           muted
           loop
           playsinline
           class="h-section h-auto w-screen object-cover absolute -z-50 bg-black">
        <source src={bgVideoFdb} type="video/mp4"/>
    </video>
    <div class="flex items-center px-4 pb-4 md:px-40 w-full">
        <div class="max-w-[100%] md:max-w-[90%] lg:max-w-[80%] xl:max-w-[70%] text-white">
            <h1 class="mb-5 text-5xl md:text-6xl lg:text-8xl font-bold">Porque en ti está la fuente de la vida</h1>
            <div class="mb-5 text-2xl md:text-3xl">
                en tu luz vemos la luz.
                <br>
                <span class="font-bold">SALMO 36:9</span>
            </div>
            <div class="flex flex-wrap gap-4">
                <button on:click={scrollIntoSection} class="btn-flat-black">
                    ¿Qué es Fuente de Bendiciones?
                </button>
                <button class="btn-flat-black">
                    ¿Dónde puedo asistir?
                </button>
            </div>
        </div>
    </div>
</section>

<section id="section-about" class="h-section flex justify-center items-center bg-white">
    <div class="container h-fit p-4">
        <h2 class="text-3xl font-light md:font-normal md:text-5xl">
            Fuente de Bendiciones es una iglesia cristiana que cree en la Biblia como la Palabra de Dios y en
            Jesucristo como el único camino para llegar a Dios.
        </h2>
        <div class="divider"></div>
        <div class="flex flex-col-reverse md:flex-row gap-4">
            <div class="w-full md:w-1/2 flex flex-col justify-center gap-4">
                <p class="text-lg md:text-2xl">
                    Nuestra misión es llevar el mensaje de salvación a todas las personas, para que puedan tener una
                    relación personal con Dios y disfrutar de una vida abundante y eterna.
                </p>
                <div class="flex flex-wrap">
                    <button class="btn-flat-black">
                        ¿Dónde puedo asistir?
                    </button>
                </div>
            </div>
            <div class="md:w-1/2">
                <img src="{descImg}" alt="descImg" class="m-auto shadow-xl rounded">
            </div>
        </div>
    </div>
</section>


<style lang="postcss">
    .btn-flat-black {
        @apply text-white bg-black rounded p-3;
    }
</style>