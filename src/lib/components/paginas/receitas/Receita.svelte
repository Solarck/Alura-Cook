<script lang="ts">
    import Card from "$lib/components/compartilhados/Card.svelte";
    import type IReceita from "$lib/interfaces/Ireceitas";

    export let receita:IReceita
</script>

<Card>
    <img
        src="/imagens\receitas\{receita.imagem}"
        alt="{receita.nome}"
        class="receita-img"
    />

    <div class="receita-info">
        <h3 class="receita-nome">Alho Assado</h3>
    </div>
</Card>

<style>
    .receita-img {
        width: 100%;
        height: 150px;
    }

    .receita-nome {
        font-size: 1.125rem;
    }

    .receita-info {
        padding: 0.75rem 0.875rem;
    }
</style>
