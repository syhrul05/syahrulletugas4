<template>
    <div class="movie-table" v-if="category">
      <h2>{{ category }} Movies</h2>
      <table>
        <thead>
          <tr>
            <th>No</th>
            <th>Title</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(movie, index) in movies[category]" :key="index">
            <td>{{ index + 1 }}</td>
            <td>{{ movie }}</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="movie-table" v-else>
      <h3>Pilih kategori film di atas untuk melihat judul film apa saja yang anda inginkan.</h3>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      category: String
    },
    data() {
      return {
        movies: {
          Horror: ['Kereta Berdarah', 'Waktu Magrib', 'KKN di Desa Penari', 'Badarauhi'],
          Romantis: ['Ancika', 'Dua Hati Biru', 'Pasutri Gaje', 'Melodate'],
          Action: ['Mencuri Raden Saleh', 'Pertaruhan', 'Hitmen', 'The Big Four']
        }
      }
    }
  }
  </script>
  
  <style scoped>
  .movie-table {
    margin-top: 20px;
    text-align: left;
  }
  
  .movie-table h2 {
    color: #333;
  }
  
  .movie-table table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 10px;
  }
  
  .movie-table th, .movie-table td {
    border: 1px solid #ddd;
    padding: 8px;
  }
  
  .movie-table th {
    background-color: #f2f2f2;
  }
  </style>
  