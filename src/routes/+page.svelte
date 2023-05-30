<!-- Inicio - / -->
<script>
    import bgVideoFdb from '$lib/videos/bg-video-fdb.mp4';
    import descImg from '$lib/images/photos/desc-img.png';
    import fdbKids from '$lib/images/fbd-kids/ministerios-carousel.png';
    import {Constants} from "../shared/constants/Constants.ts";
    import {fly} from "svelte/transition";

    const scrollIntoSection = () => {
        const sectionAbout = document.getElementById('section-about');
        scrollY = sectionAbout.offsetTop - Constants.navbarHeight;
        scroll({
            top: scrollY,
            behavior: 'smooth'
        });
    };
</script>

<!-- Seccion: Hero -->
<section class="h-section">
    <video autoplay
           muted
           loop
           playsinline
           class="min-h-[calc(100vh-66px)] h-auto w-screen object-cover absolute -z-50 bg-black">
        <source src={bgVideoFdb} type="video/mp4"/>
    </video>
    <div in:fly="{{x: -100, duration: 1500}}"
         class="flex items-center px-4 pb-4 md:px-40 w-full">
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

<!-- Seccion: About -->
<section id="section-about" class="h-section bg-white text-gray-800">
    <div class="container h-fit p-4">
        <div class="text-3xl font-light md:font-normal md:text-5xl">
            <span class="font-bold">Somos Fuente de Bendiciones,</span> una familia iglesia con los brazos abiertos a
            todas aquellas personas que
            lleguen a nosotros en cualquier circunstancia.
        </div>
        <div class="divider"></div>
        <div class="flex flex-col-reverse md:flex-row gap-4">
            <div class="w-full md:w-1/2 flex flex-col justify-center gap-4">
                <div class="text-lg md:text-2xl">
                    Nuestro propósito es amarlos, cuidarlos y guiarlos hacia un
                    nuevo estilo de vida que Jesús nos ofrece, enseñándoles el
                    camino para que ellos vayan y hagan lo mismo con otros.
                </div>
                <div class="flex flex-wrap">
                    <button class="btn-flat-black">
                        ¿Dónde puedo asistir?
                    </button>
                </div>
            </div>
            <div class="md:w-1/2">
                <img src="{descImg}" alt="descImg" class="m-auto shadow-xl rounded-xl">
            </div>
        </div>
    </div>
</section>

<!-- Seccion: Ministerios -->
<section class="h-section bg-black text-white">
    <div class="container h-fit p-4">
        <div class="text-3xl font-light md:font-normal md:text-5xl">
            Ministerios
        </div>
        <div class="divider"></div>
        <div class="flex flex-col md:flex-row gap-4">
            <div class="md:w-2/3">
                <img src="{fdbKids}" alt="fdbKids" class="m-auto w-full">
            </div>
            <div class="w-full md:w-1/2 flex flex-col justify-center gap-4">
                <div class="text-lg md:text-2xl">
                    FdB Kids es un ministerio que busca enseñar a los niños
                    sobre el amor de Dios y su palabra, de una manera divertida
                    y creativa.
                </div>
                <div class="flex flex-wrap">
                    <button class="btn-flat-black">
                        Conocer más
                    </button>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Seccion: Ubicacion -->
<section class="h-section bg-white">
</section>

<style lang="postcss">
    .btn-flat-black {
        @apply text-white bg-black rounded p-3;
    }
</style>