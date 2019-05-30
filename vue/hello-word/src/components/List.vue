<template>
  <div >
    <div>
      <input type="text" v-model="name">
      <button @click="add">添加</button>
    </div>
    <ul>
      <li v-for="(item, index) in list" :key="item.id">
        <input type="checkbox"> {{item.name}}
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'List',
    data(){
      return {
        name: '',
        newId: 3,
        list: [
          { id: 1, name: 'A' },
          { id: 2, name: 'B' },
          { id: 3, name: 'C' }
        ]
      }
    },
    methods: {
      add() {
        this.list.unshift({ id: ++this.newId, name: this.name })
        this.name = ''
      }
    }
  }
</script>

<style scoped>
  .disabled{
    cursor: not-allowed;
  }
  .active{
    cursor: pointer;
  }

  .box {
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>