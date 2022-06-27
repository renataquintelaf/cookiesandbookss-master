<template>
  <header>
    <div class="menu-esquerdo">
      <span> <RouterLink to="/">Home</RouterLink> </span>
      <span>|</span>
      <span><RouterLink to="/gerenciamento">Livros</RouterLink></span>
    </div>
    <div class="menu-direito">
      <span><RouterLink to="/tomeumcookie">Cookie</RouterLink></span>
    </div>
  </header>
</template>
<style>
header {
  height: 10%;
  color: black;
  font-size: 1.3rem;
  display: flex;
  align-items: center;
  padding-left: 20px;
  justify-content: space-between;
  background-color: var(--cor-primaria);
}
header span {
  padding: 0 20px;
  text-decoration: none;
}
header span:hover{
  background-color: var(--cor-secundaria-alt) ;
}
</style>

