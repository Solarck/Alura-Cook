<script lang="ts">
        import Tag from "./Tag.svelte";

        export let ingrediente:string
        let selecionado = false

        function AoClicar(){
            selecionado = !selecionado
        }
</script>

<button on:click={AoClicar}>
    <Tag ativa={selecionado}>{ingrediente}</Tag>
</button>

<style>
    button{
        cursor: pointer;
    }
</style>

