<template>
   <div>
    <h3>{{ titulo }}</h3>
    <input type="text" placeholder="Nome da pessoa" v-model="item">
    <button type="button" @click.Enter="adicionarItem()">Adicionar</button>
  
    <br>
    <ul>
      <li v-for="(item, index) in itens" :key="index">{{ item }}</li>
    </ul>
    <button type="button" @click="removerItem">Remover</button>
  </div>
</template>

<script>
import ListaMixim from '@/mixins/listaMixin'
import RemoverItemLista from '@/mixins/RemoverItemLista'

export default {
  name: 'ListaPessoas',
  data: () => ({
    titulo: 'Lista Pessoas'
  }),
  mixins: [ListaMixim, RemoverItemLista],

}
</script>

<style>

</style>