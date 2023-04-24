<script>
	import Header from './Header.svelte';
</script>

<div>
    <Header/>

    <main>
        <slot/>
    </main>
</div>

<style>
    main {
        margin: 0 auto;
        padding: 0 1rem;
        transition-property: width, max-width;
        transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
        transition-duration: 150ms;
    }

    @media (min-width: 640px) {
        main {
            max-width: 640px;
        }
    }

    @media (min-width: 768px) {
        main {
            max-width: 768px;
        }
    }

    @media (min-width: 1024px) {
        main {
            max-width: 1024px;
        }
    }

    @media (min-width: 1280px) {
        main {
            max-width: 1280px;
        }
    }

    @media (min-width: 1536px) {
        main {
            max-width: 1536px;
        }
    }
</style>