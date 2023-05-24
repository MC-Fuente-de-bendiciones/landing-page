<script>
    import bgVideoFdb from '$lib/videos/bg-video-fdb.mp4';
</script>

<div class="min-h-screen flex">
    <video autoplay muted loop playsinline
           class="h-screen w-screen object-cover absolute -z-50">
        <source src={bgVideoFdb} type="video/mp4" />
    </video>
    <div class="flex items-center px-4 pt-[66px] w-full">
        <div class="sm:max-w-[100%] md:max-w-[90%] lg:max-w-[80%] xl:max-w-[70%] text-white">
            <h1 class="mb-5 text-5xl md:text-6xl lg:text-8xl font-bold">Porque en ti está la fuente de la vida</h1>
            <p class="mb-5 text-2xl md:text-3xl">en tu luz vemos la luz. SALMO 36:9</p>
            <div class="flex flex-wrap gap-2">
                <button class="bg-black rounded-lg p-4">¿Qué es Fuente de Bendiciones?</button>
                <button class="bg-black rounded-lg p-4">¿Dónde puedo asistir?</button>
            </div>
        </div>
    </div>
</div>