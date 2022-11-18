<script lang="ts">
    export let valor : string
</script>

<div class="tela">
    <span>{valor}</span>
</div>

<style>
    .tela{
        display:flex;
        flex: 1;
        background-color: aliceblue;
        justify-content: flex-end;
        padding: 0px 5px;
        align-items: center;
        font-size: 1.7rem;
        overflow: hidden;
        margin: 2px 1px;

        border-top-left-radius: 5px;
        border-top-right-radius: 5px;
    }
</style>