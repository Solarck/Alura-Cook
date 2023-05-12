<script lang="ts">
    import { minhaLista } from "$lib/stores/minhaLista";
    import Tag from "../../compartilhados/Tag.svelte";

    export let ingrediente: string;
    $: selecionado = $minhaLista.includes(ingrediente);

    function AoClicar() {
        if (!selecionado) {
            minhaLista.adicionarIngrediente(ingrediente)
        } else {
            minhaLista.removerIngrediente(ingrediente)
        }
    }
</script>

<button on:click={AoClicar}>
    <Tag ativa={selecionado}>{ingrediente}</Tag>
</button>

<style>
    button {
        cursor: pointer;
    }
</style>
