<script>
export default {
  data() {
    return {
      livros: [
        {
          editora: "Uma Farsa De Amor Na Espanha",
          genero: "Português",
          autor: "908765",
        },
      ],
      novo_editora: "",
      novo_genero: "",
      novo_autor: "",
    };
  },
  methods: {
    salvar() {
      this.livros.push({
        editora: this.novo_editora,
        genero: this.novo_genero,
        autor: this.novo_autor,
      });
    },
    excluir(livro) {
      const indice = this.livros.indexOf(livro);
      this.livros.splice(indice, 1);
    },
  },
};
</script>

<template>
  <div class="container">
    <div class="left-side">
      <div class="title">
        <h2>Livros</h2>
      </div>
      <div class="form-input">
        <div class="input-dois">
          <input type="text" v-model="novo_editora" placeholder="Livro" />
        </div>
        <div class="input-tres">
          <input type="text" v-model="novo_genero" placeholder="Idioma" />
        </div>
        <div class="input-quatro">
          <input type="text" v-model="novo_autor" placeholder="Código" />
        </div>
        <button @click.enter="salvar">Salvar</button>
      </div>
    </div>
    <div class="right-side">
      <div class="list-times">
        <table>
          <thead>
            <tr>
              <th>Livro</th>
              <th>Idioma</th>
              <th>Código</th>
              <th>Opções</th>
            </tr>
          </thead>

          <tbody>
            <tr v-for="livro in livros" :key="livro.editora">
              <td>{{ livro.editora }}</td>
              <td>{{ livro.genero }}</td>
              <td>{{ livro.autor }}</td>
              <td>
                <button @click="excluir(livro)">Excluir</button>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
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
  padding: 0.5rem;
  border-radius: 10px;
  border: transparent;
}

.form-input button {
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
  color: black;
}
::placeholder {
  color: black;
  opacity: 0.5;
}
</style>
