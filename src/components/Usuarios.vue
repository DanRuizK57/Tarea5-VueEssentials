<template>
    <div>
      <h1>Lista de Usuarios</h1>

      <table class="table table-striped">
        <thead>
            <tr>
                <th scope="col">#</th>
                <th scope="col">Nombre(s)</th>
                <th scope="col">Género</th>
                <th scope="col">País</th>
                <th scope="col">Imagen</th>
                <th scope="col">Rango de Edad</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="(usuario, index) in usuarios" :key="usuario.id">
                <th scope="row">#{{ index + 1 }}</th>
                <td>{{usuario.name.title}} {{ usuario.name.first }} {{ usuario.name.last }}</td>
                <td>{{usuario.gender}}</td>
                <td>{{usuario.location.country}}</td>
                <td>
                    <img :src="usuario.picture.medium" alt="Imagen de usuario" />    
                </td>
                <td v-if="usuario.dob.age > 18">Mayor de Edad (+18)</td>
                <td v-else>Menor de Edad (-18)</td>
            </tr>
        </tbody>
</table>

    </div>
  </template>
  
  <script>
    import usuarios from '../json/users.json'

  export default {
    name: 'ListaUsuarios',
    data() {
        return {
            usuarios: []
        };
    },
    mounted() {
        this.usuarios = usuarios;
    }
  }
  </script>
  
  <style>
  
  </style>