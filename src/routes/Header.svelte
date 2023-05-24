<script>
    import fdbLogo from '$lib/images/fdb-logo.png';
    import cmnLogo from '$lib/images/cmn-logo.svg';
    import {page} from '$app/stores';
    import {afterNavigate} from "$app/navigation";

    let logoActual;
    switch ($page.url.pathname) {
        case '/cmn':
            logoActual = cmnLogo;
            break;
        default:
            logoActual = fdbLogo;
            break;
    }
    afterNavigate((navigation) => {
        switch (navigation.to.url.pathname) {
            case '/cmn':
                logoActual = cmnLogo;
                break;
            default:
                logoActual = fdbLogo;
                break;
        }
    });

    $: logo = logoActual;
</script>

<div class="absolute w-full bg-black">
    <div class="navbar container m-auto">
        <div class="navbar-start">
            <img src="{logo}" alt="Fuente de bendiciones logo"
                 class="w-[50px] h-auto">
        </div>
        <div class="navbar-end">
            <a href="/" class="btn btn-ghost text-lg text-white normal-case font-normal">Inicio</a>
            <a href="/cmn" class="btn btn-ghost text-lg text-white normal-case font-normal">Comuna</a>
        </div>
    </div>
</div>