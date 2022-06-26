<script>
export default {
  data() {
    return {
      livros: [
        {
          editora: "Editora 1",
          genero: "Genero 1",
          autor: "Autor 1",
          livro: "Livro 1",
        },
      ],
      nova_editora: "",
      novo_genero: "",
      novo_autor: "",
      novo_livro: "",
    };
  },
  methods: {
    salvar() {
      this.jogadores.push({
        nome: this.novo_,
        time: this.novo_time,
      });
    },
  },
};
</script>

<template>
  <div class="container">
    <div class="title">Livros</div>
    <div class="form-input">
      <input type="text" />
    </div>
  </div>
</template>
