<script>
import {v4 as uuidv4} from 'uuid';
export default {
    data() {
        return {
            autores: [
                {id: "33129ae6-a24a-473d-843f-49cad354acf1", nome: "Autor 1"},
                {id: "136156f9-5c1b-4fb3-aeff-ed5bd72ff176", nome: "Autor 2"},
            ]
        }
    }
}
</script>
<template>
  <div class="container">
    <div class="title">
      <h1>Autores</h1>
    </div>
    <div class="form-input">
      <input type="text" />
      <button>Salvar</button>
    </div>
    <div class="list-autores">
      <table>
        <thead>
          <tr>
            <th>ID</th>
            <th>Nome</th>
            <th>Ações</th>
          </tr>
        </thead>

        <tbody>
          <tr>
            <td>id</td>
            <td>nome</td>
            <td>
              <button>Editar</button>
              <button>Excluir</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<style></style>
