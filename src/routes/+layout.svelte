<script>
    let { children } = $props();
</script>
 
<nav class="navbar navbar-expand-sm bg-body-tertiary">
    <div class="container-fluid">
        <a class="navbar-brand" href="/#">Inicial</a>
        <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent"
            aria-expanded="false"
            aria-label="Toggle navigation"
        >
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">

            <ul class="navbar-nav">
                <li class="nav-item">
                    <a class="nav-link" href="/temporadas">Temporadas</a>
                </li>
            </ul>

            <ul class="navbar-nav">
                <li class="nav-item">
                    <a class="nav-link" href="/personagens">Personagens</a>
                </li>
            </ul>

        </div>
    </div>
</nav>
 
{@render children()}