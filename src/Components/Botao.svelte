<script lang="ts">
    export let texto : string
    export let triplo: boolean = false
    export let duplo : boolean = false
    export let operacao : boolean = false
    export let destaque : boolean = false
    export let onClick: (valor:string) => void = () => {}
</script>

<button class="botao" 
    class:triplo 
    class:duplo 
    class:operacao
    class:destaque
    on:click={()=>onClick(texto)}>
    {texto}
</button>

<style>
    .botao{
        margin: 0;
        border: 1px solid var(--cor-fundo);
        flex-basis: 25%;
    }
    .triplo{
        flex-basis: 75%;
    }
    .duplo{
        flex-basis: 50%;
    }
    .destaque{
        background-color: #4f5cb7;
        color: white
    }
    .operacao{
        background-color: #2fb7b0;
        color: white
    }
</style>