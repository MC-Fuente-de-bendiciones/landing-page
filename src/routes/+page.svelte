<script>
    import bgVideoFdb from '$lib/videos/bg-video-fdb.mp4';
</script>

<div class="hero min-h-screen">
    <video autoplay muted loop playsinline
           class="max-h-full max-w-full h-full w-full object-cover -z-50">
        <source src={bgVideoFdb} type="video/mp4" />
    </video>
    <div class="hero-overlay bg-opacity-60">
    </div>
    <div class="hero-content text-center text-neutral-content">
        <div class="max-w-md">
            <h1 class="mb-5 text-5xl xl:text-8xl font-bold">Bienvenido a casa</h1>
            <p class="mb-5">Porque en ti está la fuente de la vida; en tu luz vemos la luz. SALMO 36:9</p>
            <button class="btn btn-primary">Get Started</button>
        </div>
    </div>
</div>