<script>
    import Header from './Header.svelte';
    import "../app.css";
</script>

<div>
    <Header/>

    <main class="pt-[66px]">
        <slot/>
    </main>
</div>