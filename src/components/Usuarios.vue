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
            <tr>
                <th scope="row">1</th>
                <td>{{nombre}}</td>
                <td>{{genero}}</td>
                <td>{{pais}}</td>
                <td>
                    <img :src="imagen" alt="Imagen de usuario" />    
                </td>
                <td>{{rangoEdad}}</td>
            </tr>
            <tr>
                <th scope="row">2</th>
                <td>Jacob</td>
                <td>Hombre</td>
                <td>Inglaterra</td>
                <td>Imagen</td>
                <td>Mayor de Edad (+18)</td>
            </tr>
            <tr>
                <th scope="row">3</th>
                <td>Jeny</td>
                <td>Mujer</td>
                <td>Australia</td>
                <td>Imagen</td>
                <td>Mayor de Edad (+18)</td>
            </tr>
            <tr>
                <th scope="row">4</th>
                <td>Pepe</td>
                <td>Hombre</td>
                <td>España</td>
                <td>Imagen</td>
                <td>Mayor de Edad (+18)</td>
            </tr>
            <tr>
                <th scope="row">5</th>
                <td>Juan</td>
                <td>Hombre</td>
                <td>México</td>
                <td>Imagen</td>
                <td>Mayor de Edad (+18)</td>
            </tr>
            <tr>
                <th scope="row">6</th>
                <td>Catalina</td>
                <td>Mujer</td>
                <td>Argentina</td>
                <td>Imagen</td>
                <td>Mayor de Edad (+18)</td>
            </tr>
            <tr>
                <th scope="row">7</th>
                <td>Valentina</td>
                <td>Mujer</td>
                <td>Chile</td>
                <td>Imagen</td>
                <td>Mayor de Edad (+18)</td>
            </tr>
            <tr>
                <th scope="row">8</th>
                <td>José</td>
                <td>Hombre</td>
                <td>Uruguay</td>
                <td>Imagen</td>
                <td>Mayor de Edad (+18)</td>
            </tr>
            <tr>
                <th scope="row">9</th>
                <td>Joao</td>
                <td>Hombre</td>
                <td>Brasil</td>
                <td>Imagen</td>
                <td>Mayor de Edad (+18)</td>
            </tr>
            <tr>
                <th scope="row">10</th>
                <td>Angélica</td>
                <td>Mujer</td>
                <td>Colombia</td>
                <td>Imagen</td>
                <td>Mayor de Edad (+18)</td>
            </tr>
        </tbody>
</table>

    </div>
  </template>
  
  <script>
    import usuarios from '../json/users.json'

    const miss = usuarios.filter(usuario => usuario.name.title === "Miss")
    let nombre = miss[3].name.title + " " + miss[3].name.first + " " + miss[3].name.last
    let genero = miss[3].gender
    let pais = miss[3].location.country
    let imagen = miss[3].picture.medium
    let rangoEdad;

    if (miss[3].dob.age > 18){
        rangoEdad = "Mayor de edad (+18)"
    } else {
        rangoEdad = "Menor de edad (-18)"
    }

  export default {
    name: 'ListaUsuarios',
    data() {
        return {
            nombre: "",
            genero: "",
            pais: "",
            imagen: "",
            rangoEdad: ""
        };
    },
    mounted() {
        this.nombre = nombre;
        this.genero = genero;
        this.pais = pais;
        this.imagen = imagen;
        this.rangoEdad = rangoEdad;
    }
  }
  </script>
  
  <style>
  
  </style>