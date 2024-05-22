<template>
  <div class="app">
    <div class="frame">
      <div class="header">
        <h1>Daftar Film Bioskop</h1>
      </div>
      <div class="content">
        <ButtonGroup @update-category="selectedCategory = $event" />
        <MovieTable :category="selectedCategory" />
      </div>
    </div>
  </div>
</template>

<script>
import ButtonGroup from './components/ButtonGroup.vue'
import MovieTable from './components/MovieTable.vue'

export default {
  components: {
    ButtonGroup,
    MovieTable
  },
  data() {
    return {
      selectedCategory: ''
    }
  }
}
</script>

<style>
html, body {
  height: 100%;
  margin: 0;
  background-color: #000; /* Mengubah warna latar belakang menjadi hitam */
  background-image: url('http://jadiberita.com/wp-content/uploads/2016/05/054748900_1427107006-Bangku-bioskop-150323.jpg'); /* Ganti path dengan lokasi gambar latar belakang Anda */
  background-size: cover; /* Memastikan gambar latar belakang mengisi seluruh area */
  background-position: center; /* Posisi gambar latar belakang di tengah */
  font-family: Arial, sans-serif;
}

.app {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}

.frame {
  background-color: rgba(255, 255, 255, 0.9); /* Menggunakan transparansi pada latar belakang untuk memberi kesan studio yang terang */
  padding: 20px;
  border-radius: 20px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
  text-align: center;
  width: 90%;
  max-width: 1000px;
}

.frame .header {
  margin-bottom: 20px;
}

.frame h1 {
  margin: 0;
  font-size: 28px;
  color: #333;
}

.content {
  margin-top: 20px;
}
</style>
