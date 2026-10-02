<script setup>
import ProductCard from '../components/ProductCard.vue'

const daftarProduk = [
  {
    id: 1,
    nama: 'Kaos Sekolah',
    harga: 75000,
    gambar: '/image/kaos.jpg'
  },
  {
    id: 2,
    nama: 'Topi Sekolah',
    harga: 35000,
    gambar: '/image/topi.jpg'
  },
  {
    id: 3,
    nama: 'Tas Sekolah',
    harga: 120000,
    gambar: '/image/tas.jpg'
  }
]
</script>

<template>
  <main>
    <div class="grid">
      <ProductCard
        v-for="produk in daftarProduk"
        :key="produk.id"
        :nama="produk.nama"
        :harga="produk.harga"
        :gambar="produk.gambar"
      />
    </div>
  </main>
</template>

<style scoped>
main {
  padding: 20px;
}

.grid {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
}
</style>