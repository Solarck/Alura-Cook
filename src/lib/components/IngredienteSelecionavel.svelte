<script lang="ts">
    import { minhaLista } from "$lib/stores/minhaLista";
    import Tag from "./Tag.svelte";

    export let ingrediente: string;
    let selecionado = false;

    function AoClicar() {
        selecionado = !selecionado;

        if (selecionado) {
            $minhaLista = [...$minhaLista, ingrediente];
        } else {
            $minhaLista = $minhaLista.filter((item) => item !== ingrediente);
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
