<template>
  <div id="app">
    <h1>Biodata Diri</h1>
    <div class="biodata-container">
      <img :src="biodata.foto" alt="Foto Profil" class="profile-pic"/>
      <div class="biodata-info">
        <p><strong>Nama:</strong> <span :style="{ color: textColor }">{{ biodata.nama }}</span></p>
        <p><strong>Umur:</strong> <span :style="{ color: textColor }">{{ biodata.umur }}</span></p>
        <p><strong>Alamat:</strong> <span :style="{ color: textColor }">{{ biodata.alamat }}</span></p>
        <p><strong>Hobi:</strong> <span :style="{ color: textColor }">{{ biodata.hobi }}</span></p>
        <p><strong>Pendidikan:</strong> <span :style="{ color: textColor }">{{ biodata.pendidikan }}</span></p>
      </div>
    </div>
    <button @click="changeColor">Ubah Warna Teks</button>
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
        foto: 'gallery/WhatsApp Image 2024-06-24 at 19.16.31_c59cc517.jpg' // Ganti dengan URL foto Anda
      },
      textColor: '#2c3e50' // Warna default
    };
  },
  methods: {
    changeColor() {
      const colors = ['#2c3e50', '#e74c3c', '#3498db', '#2ecc71', '#f1c40f'];
      this.textColor = colors[Math.floor(Math.random() * colors.length)];
    }
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

.biodata-container {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 20px;
}

.profile-pic {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  object-fit: cover;
  margin-right: 20px;
}

.biodata-info {
  text-align: left;
}

button {
  margin-top: 20px;
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}
</style>
