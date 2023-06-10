<template>
    <div class="container">
      <table class="table table-sm table-striped table-bordered text-center">
        <thead>
          <tr>
            <th>Nombre</th>
            <th>Fecha</th>
            <th>Hora</th>
            <th>Cancelaciones</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="otrosUsuarios in otrosUsuarios" :key="otrosUsuarios.id">
            <td>       
              <div class="d-flex align-items-center ">
              <img :src="otrosUsuarios.foto" alt="Foto de usuario" class="rounded-circle mr-2" style="width: 30px; height: 30px;">
              <span>{{ otrosUsuarios.nombre }}</span>
            </div>
            </td>
            <td>{{ otrosUsuarios.fecha }}</td>
            <td>{{ otrosUsuarios.hora }}</td>
            <td>
              <span v-if="otrosUsuarios.cancelaciones" class="success">&#10004;</span>
              <span v-else class="danger">&#10008;</span>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  export default {
    name: 'OtrosUsuarios',
    data() {
      return {
        otrosUsuarios:[
            {
                id: 5,
                nombre: "Pedro Gómez",
                fecha: "26-10-2023",
                hora: "14:30",
                cancelaciones: true,
                foto: "https://i.pravatar.cc/150?img=15",
              },
              {
                id: 6,
                nombre: "Laura Fernández",
                fecha: "26-10-2023",
                hora: "16:45",
                cancelaciones: false,
                foto: "https://i.pravatar.cc/150?img=25",
              },
              {
                id: 7,
                nombre: "José Martinez",
                fecha: "27-10-2023",
                hora: "10:00",
                cancelaciones: false,
                foto: "https://i.pravatar.cc/150?img=35",
              },
              {
                id: 8,
                nombre: "Sofía Rodríguez",
                fecha: "27-10-2023",
                hora: "11:30",
                cancelaciones: false,
                foto: "https://i.pravatar.cc/150?img=45",
              },
            ],    
      };
    },
  };
  </script>
  
  <style>
  table {
      width: 100%;
      border-collapse: collapse;
      background-color: #fff;
      border: 1px solid #dee2e6;
      box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
  }
  
  th, td {
      background-color: #343a40;
      text-align: center;
      padding: 10px;
      font-size: 20px;
      vertical-align: middle;
  }
  
  th {
      background-color: #333;
      color: #333;
  }
  
  </style>