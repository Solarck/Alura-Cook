<script lang="ts">
    import "../app.css";
    import Cabecalho from "../lib/components/Cabecalho.svelte";
    import MinhaLista from "../lib/components/MinhaLista.svelte";
</script>

<svelte:head>
    <title>Alura Cook</title>
    <link rel="shortcut icon" href="/favincon.png" type="image/x-icon" />
</svelte:head>

<div class="container-principal">
    <Cabecalho />

    <div class="estilo-principal">
        <div class="minha-lista-container">
            <MinhaLista />
        </div>
    </div>
</div>

<style>
    .container-principal {
        display: flex;
        flex-direction: column;
        min-height: 100vh;
    }

    .estilo-principal {
        text-align: center;
        padding: 0 5vw 3.375rem;
        flex: 1;
    }

    .minha-lista-container {
        margin-bottom: 2rem;
    }

    .divisoria {
        width: 40vw;
        height: 2px;
        background-color: var(--verde);
        margin: 0 auto;
    }

    .info {
        margin-bottom: 3.375rem;
    }

    .info > p {
        line-height: 2rem;
    }
</style>
