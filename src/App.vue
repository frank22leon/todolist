<template>
  <div>
    <h1>Crea una nueva tarea</h1>

    <div class="input-control">
      <label>Tarea</label>
      <input
        type="text"
        placeholder="Ingrese un nuevo Item"
        v-model="nuevaActividad"
      />
      <button @click="agregarNuevoItem">Crear</button>
    </div>

    <h1>Lista</h1>

    <ul>
      <li v-for="(actividad, $i) in actividades" :key="$i">
        {{ actividad }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    nuevaItems: "",
    actividades: [],
  }),
  methods: {
    agregarNuevoItem() {
      this.actividades.push(this.nuevaItems);
      this.nuevaItems = "";
    },
  },
};
</script>

<style scoped></style>