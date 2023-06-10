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
          <tr v-for="masUsuarios in masUsuarios" :key="masUsuarios.id">
            <td>       
              <div class="d-flex align-items-center ">
              <img :src="masUsuarios.foto" alt="Foto de usuario" class="rounded-circle mr-2" style="width: 30px; height: 30px;">
              <span>{{ masUsuarios.nombre }}</span>
            </div>
            </td>
            <td>{{ masUsuarios.fecha }}</td>
            <td>{{ masUsuarios.hora }}</td>
            <td>
              <span v-if="masUsuarios.cancelaciones" class="success">&#10004;</span>
              <span v-else class="danger">&#10008;</span>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  export default {
    name: 'MasUsuarios',
    data() {
      return {
        masUsuarios:[
            {
                id: 9,
                nombre: "Sofía Herrera",
                fecha: "20-12-2023",
                hora: "10:00",
                cancelaciones: true,
                foto: "https://i.pravatar.cc/150?img=37",
                },
            {
                id: 10,
                nombre: "Gabriel Montes",
                fecha: "25-12-2023",
                hora: "12:30",
                cancelaciones: true,
                foto: "https://i.pravatar.cc/150?img=40",
            },
            {
                id: 11,
                nombre: "Carolina Ríos",
                fecha: "30-12-2023",
                hora: "14:45",
                cancelaciones: false,
                foto: "https://i.pravatar.cc/150?img=45",
            },
            {
                id: 12,
                nombre: "Luis Medina",
                fecha: "05-01-2024",
                hora: "16:00",
                cancelaciones: true,
                foto: "https://i.pravatar.cc/150?img=50",
                    },
        ]
          
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