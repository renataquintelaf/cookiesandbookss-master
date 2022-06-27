<template>
  <header>
    <div class="menu">
      <span> <RouterLink to="/">Home</RouterLink> </span>
      <span>|</span>
      <span><RouterLink to="/gerenciamento">Livros</RouterLink></span>
    </div>
  </header>
</template>
<style>
header {
  height: 10%;
  background-color: rgb(171, 76, 135);
  color: black;
  font-size: 1.3rem;
  display: flex;
  align-items: center;
  padding-left: 20px;
  border-radius: 10px;
}
header span {
  padding: 0 20px;
  text-decoration: none;
}
</style>
