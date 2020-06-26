<template>
  <div id="app">
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css" integrity="sha384-9aIt2nRpC12Uk9gS9baDl411NQApFmC26EwAOH8WgZl5MYYxFfc+NcPb1dKGj7Sk" crossorigin="anonymous">
    <div class="container">
      <div class="row justify-content-center">
        <h1 class="mt-5 mb-5"><strong>Tabla de Usuarios</strong></h1>
          <table class="table">
          <thead class="thead-dark">
            <tr>
              <th scope="col">#</th>
              <th scope="col">Nombre</th>
              <th scope="col">Apellido</th>
              <th scope="col">RUN</th>
              <th scope="col">Nacimiento</th>
              <th scope="col">Edad</th>
            </tr>
          </thead>
          <tbody>
            <tr  v-for="(item, index) in items" :key="index">
              <th scope="row">{{ index+1 }}</th>
              <td>{{ item.name }}</td>
              <td>{{ item.last }}</td>
              <td>{{ item.run }}</td> 
              <td>{{ item.date }}</td>
              <td>{{ item.age }}</td>  
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data(){
    return{
    items: [{
      name:'María',
      last: 'Rodríguez',
      run: '6.543.210-1',
      date: '15-12-1949',
      age: '69',
    },
    {
      name:'José',
      last: 'Perez',
      run: '10.345.678-9',
      date: '20-01-1965',
      age: '55',
    },
     {
      name:'Manuel',
      last: 'Lopez',
      run: '16.455.678-5',
      date: '15-12-1986',
      age: '33',
    }
    ]}
  }
}
</script>
