<script lang="ts">
    import Tag from "$lib/components/compartilhados/Tag.svelte";
    import { minhaLista } from "$lib/stores/minhaLista";

    export let ingrediente: string;

    function removerIngrediente (){
        minhaLista.removerIngrediente(ingrediente)
    }
</script>

<div class="meu-ingrediente-container">
    <Tag ativa={true}>
        <button class="close" on:click={removerIngrediente}></button>
        {ingrediente}
    </Tag>
</div>

<style>
    .meu-ingrediente-container {
        position: relative;
    }
   
    .close {
        background-image: url("icones/close.svg");
        height: 10px;
        width: 10px;
        cursor: pointer;
 
        position: absolute;
        top: 4px;
        right: 4px;
    }
</style>