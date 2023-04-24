<script>
    import fb_logo from '$lib/images/fb-logo.png';
</script>

<nav>
    <img src="{fb_logo}"
         alt="Fuente de bendiciones"
         class="fb-logo">
    <div class="menu-items">
        <a href="/">Inicio</a>
        <a href="about">Quienes somos</a>
        <a>Doctrina</a>
        <a>Ministerios</a>
        <a>Eventos</a>
        <a>Ubicación</a>
    </div>
</nav>

<style>
    nav {
        background-color: #FFFFFF20;
        display: flex;
        align-items: center;
        border-radius: 1rem;
        width: 100%;
    }

    a:link, a:visited {
        text-decoration: inherit;
        color: inherit;
        cursor: pointer;
    }

    .menu-items {
        display: flex;
        gap: 3rem;
        margin-left: 3rem;
        color: white;
    }

    .fb-logo {
        width: 75px;
        height: 75px;
    }
</style>