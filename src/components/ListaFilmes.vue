<template>
  <div>
    <h3>{{ titulo }}</h3>
    <input type="text" placeholder="Nome do filme" v-model="item">
    <button type="button" @click.Enter="adicionarItem()">Adicionar</button>
  
    <br>
    <ul>
      <li v-for="(item, index) in itens" :key="index">{{ item }}</li>
    </ul>
    <button type="button" @click="removerItem">Remover</button>
  </div>
</template>

<script>
import listaMixin from '@/mixins/listaMixin'
import RemoverItemLista from '@/mixins/RemoverItemLista'

export default {
  name: 'ListaFilmes',
  data: () => ({
    titulo: 'Lista Filmes'
  }),
  mixins: [listaMixin, RemoverItemLista],
  created() {
    console.log('ListaFilmes Criado')
  }
}
</script>

<style>

</style>