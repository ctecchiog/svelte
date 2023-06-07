<script>
    import UTFPRlogo from "../../assets/logo.svg";
    export let acao;
    export let clientHeight;
</script>
<header class="d-flex navbar" bind:clientHeight={clientHeight}>
    <nav class="andar1">
        <div class="universidade">
            <img id="logo-utfpr" src={UTFPRlogo} alt="Logo UTFPR"/>
            <p class="nome-utfpr">UNIVERSIDADE TECNOLÓGICA FEDERAL DO PARANÁ</p>
        </div>
        <div>
            <div class="notificacao">
                <p class="not">1</p>
            </div>
        </div>
    </nav>
    <div class="prae">
        
        <button class="botao" on:click={acao}>
            <div class="linha"></div>
            <div class="linha"></div>
            <div class="linha"></div>
        </button>
        <div>
            <div>
                PRAE
            </div>
            <div>
                Página do Professor
            </div>
        </div>
    </div>
</header>
<style>
.d-flex{
    display: flex;
}
.navbar{
    flex-direction: column;
    padding: 1rem;
}

.andar1{
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.universidade{
    display: flex;
    align-items: center;
}

#logo-utfpr{
    width: 100px;
}
.nome-utfpr{
    margin: 0;
    font-size: 12px;
    max-width: 207px;
    margin-left: 1rem;
}
.notificacao{
    background-color: #0C326F;
    padding: 0.5rem;
    border-radius: 50%;
    display: flex;
    width: 35px;
    height: 35px;
    justify-content: center;
    align-items: center;
}
.not{
    color: #fff; 
    margin: 0;
}
.linha{
    width: 20px;
    height: 2px;
    background-color: #0C326F;
}
.botao{
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    border: 0;
    height: 25px;
}
.prae{
    display: flex;
    align-items: center;
}
</style>