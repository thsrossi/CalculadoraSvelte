<script lang="ts">
    import CalculadoraModel from "../model/CalculadoraModel";
    import Botao from "./Botao.svelte";
    import Linha from "./Linha.svelte";
    import Tela from "./Tela.svelte";

    function numeroDigitado(num : string){
        calc = calc.numeroDigitado(num)
    }

    function pontoDigitado(){
        calc = calc.pontoDigitado()
    }
    
    function operacaoDigitada(operacao:string){
        calc = calc.operacaoDigitada(operacao)
    }

    function calcular(){
        calc = calc.calcular()
    }

    function limpar(){
        calc = calc.limpar()
    }

    let calc = new CalculadoraModel()
</script>
<div class="calculadora">
    <Tela valor={calc.valor} />
    <Linha>
        <Botao texto="AC" triplo destaque onClick={limpar}/>
        <Botao texto="/" operacao onClick={operacaoDigitada}/>
    </Linha>
    <Linha>
        <Botao texto="7" onClick={numeroDigitado}/>
        <Botao texto="8" onClick={numeroDigitado}/>
        <Botao texto="9" onClick={numeroDigitado}/>
        <Botao operacao texto="*" onClick={operacaoDigitada}/>
    </Linha>
    <Linha>
        <Botao texto="4" onClick={numeroDigitado}/>
        <Botao texto="5" onClick={numeroDigitado}/>
        <Botao texto="6" onClick={numeroDigitado}/>
        <Botao operacao texto="+" onClick={operacaoDigitada}/>
    </Linha>
    <Linha>
        <Botao texto="1" onClick={numeroDigitado}/>
        <Botao texto="2" onClick={numeroDigitado}/>
        <Botao texto="3" onClick={numeroDigitado} />
        <Botao operacao texto="-" onClick={operacaoDigitada}/>
    </Linha>
    <Linha>
        <Botao duplo texto="0" onClick={numeroDigitado}/>
        <Botao texto="," onClick={pontoDigitado}/>
        <Botao destaque texto="=" onClick={calcular}/>
    </Linha>
</div>

<style>
    .calculadora{
        background-color: var(--cor-fundo);
        height: 220px;
        width: 150px;
        padding: 10px;
        border-radius: 10px;
        display:flex;
        flex-direction: column
    }
</style>