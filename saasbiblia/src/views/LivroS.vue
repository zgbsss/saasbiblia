<script>
import { v4 as uuidv4 } from "uuid";
export default {
  data() {
    return {
      livros: [
        { id: "33129ae6-a24a-473d-843f-49cad354acf1", nome: "Livro 1", categoria: "Categoria 1", editora: "Editora 1", quantidade: "1", preço: "1"},
        { id: "136156f9-5c1b-4fb3-aeff-ed5bd72ff176", nome: "Livro 2", categoria: "Categoria 2", editora: "Editora 2", quantidade: "2", preço: "2"},
      ],
      novo_livro: "",
      novo_categoria: "",
      novo_editora: "",
      novo_quantidade: "",
      novo_preço: "",
    };
  },
  methods: {
    salvar() {
      if (this.novo_livro !== "") {
        const novo_id = uuidv4();
        this.livros.push({
          id: novo_id,
          nome: this.novo_livro,
          categoria: this.novo_categoria,
          editora: this.novo_editora,
          quantidade: this.novo_quantidade,
          preço: this.novo_preço
        });
        this.novo_livro = "";
        this.novo_categoria = "";
        this.novo_editora = "";
        this.novo_quantidade = "";
        this.novo_preço = "";
      }
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
    <div class="title">
      <h1>Livros</h1>
    </div>
    <div class="form-input">
      <input type="text" v-model="novo_livro" />
      <input type="text" v-model="novo_categoria" />
      <input type="text" v-model="novo_editora" />
      <input type="number" v-model="novo_quantidade" />
      <input type="number" v-model="novo_preço" />
      <button @click="salvar">Salvar</button>
    </div>
    <div class="list-livros">
      <table>
        <thead>
          <tr>
            <th>ID</th>
            <th>Título</th>
            <th>Categoria</th>
            <th>Editora</th>
            <th>Quantidade</th>
            <th>Preço</th>
            <th>Ação</th>
          </tr>
        </thead>

        <tbody>
          <tr v-for="livro in livros" :key="livro.id">
            <td>{{ livro.id }}</td>
            <td>{{ livro.nome }}</td>
            <td>{{ livro.categoria }}</td>
            <td>{{ livro.editora }}</td>
            <td>{{ livro.quantidade }}</td>
            <td>{{ livro.preço }}</td>
            <td>
              <button @click="excluir(livro)">Excluir</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<style></style>