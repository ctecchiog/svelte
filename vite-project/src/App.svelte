<script>
  import Navbar from "./lib/Componentes/navbar.svelte";
  import Sidebar from "./lib/Componentes/sidebar.svelte";
  let mostraSidebar = false;
  function acao(){
    mostraSidebar = !mostraSidebar;
  }
  let alturaNavbar;
</script>

<Navbar acao={acao} bind:clientHeight={alturaNavbar}>
  
</Navbar>
{
  #if mostraSidebar
}
<Sidebar alturaNavbar={alturaNavbar}>

</Sidebar>
{
  /if
}
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA