<script>
    export let alturaNavbar;
    let estado = [false, false, false, false, false];
    function mudaEstado(posicao){
        estado[posicao] = !estado[posicao];
    }
</script>
<div class="sidebar" style:top={alturaNavbar}>
        <button on:click={()=>mudaEstado(0)}>
            Aprovar cadastro de estagiário
        </button>
        <button on:click={()=>mudaEstado(1)}>
            Visualizar estagiários
        </button>
        {#if estado[1]      
        }
        <button class="submenu">Ativos</button>
        <button class="submenu">Inativos</button>
        <button class="submenu">Todos</button>
        {/if}
        <button on:click={()=>mudaEstado(2)}>
            Atualizar estagiários
        </button>
        <button on:click={()=>mudaEstado(3)}>
            Visualizar relatórios
        </button>
        <button on:click={()=>mudaEstado(4)}>
            Cadastrar empresa
        </button>
</div>
<style>
    *{
        margin: 0;
        padding: 0;
    }
    .sidebar{
        display: flex;
        flex-direction: column;
        position: absolute;
        background-color: rgb(250, 244, 244);
        border: 2px solid #aaa;
    }
    button{
        padding: 1rem;
        border-bottom: 1px solid #bbb;
    }
    .submenu{
        margin-left: 2rem;
    }
</style>