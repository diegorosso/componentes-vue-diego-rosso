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
          <tr v-for="usuario in usuarios" :key="usuario.id">
            <td>       
              <div class="d-flex align-items-center ">
              <img :src="usuario.foto" alt="Foto de usuario" class="rounded-circle mr-2" style="width: 30px; height: 30px;">
              <span>{{ usuario.nombre }}</span>
            </div>
            </td>
            <td>{{ usuario.fecha }}</td>
            <td>{{ usuario.hora }}</td>
            <td>
              <span v-if="usuario.cancelaciones" class="success">&#10004;</span>
              <span v-else class="danger">&#10008;</span>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ListaUsuarios',
    data() {
      return {
        usuarios:[
                  {
                      id: 1,
                      nombre:"Diego Rosso",
                      fecha: "25-10-2023",
                      hora: "11:00",
                      cancelaciones: false,
                      foto: "https://i.pravatar.cc/150?img=3"
  
                  },
                  {
                      id: 2,
                      nombre:"Carlos Dale",
                      fecha: "02-12-2023",
                      hora: "13:00",
                      cancelaciones: true,
                      foto: "https://i.pravatar.cc/150?img=53"
  
                  },
                  {
                      id: 3,
                      nombre: "María López",
                      fecha: "25-10-2023",
                      hora: "17:15",
                      cancelaciones: false,
                      foto: "https://i.pravatar.cc/150?img=5"
                  },
                  {
                      id: 4,
                      nombre: "Juana Pérez",
                      fecha: "25-10-2023",
                      hora: "18:10",
                      cancelaciones: true,
                      foto: "https://i.pravatar.cc/150?img=10"
                  },
                  ],
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