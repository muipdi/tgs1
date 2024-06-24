<template>
    <div id="app">
      <h1>Biodata Diri</h1>
      <img src='foto profil' alt="Foto Profil" class="profile-pic"/>
      <p><strong>Nama:</strong> {{ biodata.nama }}</p>
      <p><strong>Umur:</strong> {{ biodata.umur }}</p>
      <p><strong>Alamat:</strong> {{ biodata.alamat }}</p>
      <p><strong>Hobi:</strong> {{ biodata.hobi }}</p>
      <p><strong>Pendidikan:</strong> {{ biodata.pendidikan }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'App',
    data() {
      return {
        biodata: {
          nama: 'M. Irfan Pebriadi',
          umur: '20',
          alamat: 'Panam',
          hobi: 'Play Gamers',
          pendidikan: 'S1 Teknik Informatika, Universitas Islam Riau',
          foto: 'gallery/WhatsApp Image 2024-06-24 at 19.16.31_c59cc517 ' // Ganti dengan URL foto Anda
        }
      };
    }
  }
  </script>
  
  <style scoped>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  
  .profile-pic {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 20px;
  }
  </style>
  