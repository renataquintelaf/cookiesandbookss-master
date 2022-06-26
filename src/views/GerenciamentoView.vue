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
      if (this.novo_editora !== "") {
        this.livros.push({
          nome: this.novo_editora,
        });
        this.novo_editora = "";
      }
      if (this.novo_genero !== "") {
        this.livros.push({
          nome: this.novo_genero,
        });
        this.novo_genero = "";
      }
      if (this.novo_autor !== "") {
        this.livros.push({
          nome: this.novo_autor,
        });
        this.novo_autor = "";
      }
      if (this.novo_livro !== "") {
        this.livros.push({
          nome: this.novo_livro,
        });
        this.novo_livro = "";
      }
    },
  },
};
</script>

<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de Livros</h2>
    </div>
    <div class="form-input">
      <input type="text" v-model="novo_editora" @keydown.enter="salvar" />
      <div class="input-um">
        <input type="text" v-model="novo_editora" />
      </div>
      <div class="input-dois">
        <input type="text" v-model="novo_genero" />
      </div>
      <div class="input-tres">
        <input type="text" v-model="novo_autor" />
      </div>
      <div class="input-quatro">
        <input type="text" v-model="novo_livro" />
      </div>
      <button @click="salvar">Salvar</button>
    </div>
    <div class="list-times">
      <table>
        <thead>
          <tr>
            <th>Editora</th>
            <th>Genero</th>
            <th>Autor</th>
            <th>Livro</th>
            <th>Opções</th>
          </tr>
        </thead>

        <tbody>
          <tr v-for="livro in livros" :key="livro.editora">
            <td>{{ livro.editora }}</td>
            <td>{{ livro.genero }}</td>
            <td>{{ livro.novo_autor }}</td>
            <td>{{ livro.novo_livro }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<style>
.title {
  text-align: center;
  margin: 2rem 0;
  font-size: 150%;
}

.form-input {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 2rem 0;
  border-radius: 30px;
  padding: 2rem;
}
.form-input input {
  width: 80%;
  padding: 0.5rem;
  border-radius: 10px;
  background-color: #a67794;
  border: transparent;
}

.form-input button {
  background-color: rgb(166, 119, 148);
  border-radius: 20%;
}
input,
button {
  padding: 0.6rem;
  border: transparent;
}

.list-times {
  display: flex;
  justify-content: center;
}

table {
  width: 50%;
  border-collapse: collapse;
  margin: 0 auto;
  border: transparent;
  font-size: 1rem;
  text-align: center;
}

table thead {
  background-color: rgb(166, 119, 148);
  color: white;
}
</style>
