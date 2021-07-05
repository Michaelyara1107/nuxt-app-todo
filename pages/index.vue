<template>
  <div>
    <div class="p-2">
      <input v-model="titulo" @keypress.enter="agregarTarea" class="py-1 px-3 rounded-sm bg-blue-200 focus:outline-none w-full border-gray-400" type="text">
      <button @click="agregarTarea" class="bg-black text-white py-2 px-4 rounded-full mt-2 btn-asombroso">Agregar tarea</button>
    </div>
    <Card v-for="tarea in tareas" :titulo="tarea.titulo" />
  </div>
</template>

<script>
export default {

  data() {

    return {
      tareas: [
        {
          titulo: 'Aprender Nuxt'
        },
        {
          titulo: 'Hacer policias de la API completa'
        }
      ],
      titulo: ''
    }

  },
  methods: {
    agregarTarea() {
      if( this.titulo === '' ) {
        alert('Error por favor ingresa una información');
        return;
      }
      this.tareas.push({ titulo: this.titulo });
      this.titulo = '';
    }
  }

}
</script>
<style lang="sass" scoped>
  .btn-asombroso
    &:hover
      background-color: #3b3b3b
    width: 100%
</style>
