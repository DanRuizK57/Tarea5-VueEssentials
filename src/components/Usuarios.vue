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
            </tr>
        </thead>
        <tbody>
            <tr>
                <th scope="row">1</th>
                <td>{{nombre}}</td>
                <td>Hombre</td>
                <td>Estados Unidos</td>
                <td>Imagen</td>
            </tr>
            <tr>
                <th scope="row">2</th>
                <td>Jacob</td>
                <td>Hombre</td>
                <td>Inglaterra</td>
                <td>Imagen</td>
            </tr>
            <tr>
                <th scope="row">3</th>
                <td>Jeny</td>
                <td>Mujer</td>
                <td>Australia</td>
                <td>Imagen</td>
            </tr>
            <tr>
                <th scope="row">4</th>
                <td>Pepe</td>
                <td>Hombre</td>
                <td>España</td>
                <td>Imagen</td>
            </tr>
            <tr>
                <th scope="row">5</th>
                <td>Juan</td>
                <td>Hombre</td>
                <td>México</td>
                <td>Imagen</td>
            </tr>
            <tr>
                <th scope="row">6</th>
                <td>Catalina</td>
                <td>Mujer</td>
                <td>Argentina</td>
                <td>Imagen</td>
            </tr>
            <tr>
                <th scope="row">7</th>
                <td>Valentina</td>
                <td>Mujer</td>
                <td>Chile</td>
                <td>Imagen</td>
            </tr>
            <tr>
                <th scope="row">8</th>
                <td>José</td>
                <td>Hombre</td>
                <td>Uruguay</td>
                <td>Imagen</td>
            </tr>
            <tr>
                <th scope="row">9</th>
                <td>Joao</td>
                <td>Hombre</td>
                <td>Brasil</td>
                <td>Imagen</td>
            </tr>
            <tr>
                <th scope="row">10</th>
                <td>Angélica</td>
                <td>Mujer</td>
                <td>Colombia</td>
                <td>Imagen</td>
            </tr>
        </tbody>
</table>

    </div>
  </template>
  
  <script>
    import usuarios from '../json/users.json'

    const miss = usuarios.filter(usuario => usuario.name.title === "Miss")
    const nombre = miss[3].name.title
  export default {
    name: 'ListaUsuarios',
    data() {
        return {
            nombre: ""
        };
    },
    mounted() {
        this.nombre = nombre;
    }
  }
  </script>
  
  <style>
  
  </style>