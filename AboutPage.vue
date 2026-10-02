<template>
  <main>
    <!-- Judul -->
    <div class="Judul">
      <h1>Tentang kami</h1>
    </div>

    <!-- Cerita Kami -->
    <div class="Cerita">
      <div class="IsiCerita">
        <h1>Cerita Kami</h1>

        <p>
          Onlineshop ini dikelola langsung oleh siswa SMK Yadika Soreang
          jurusan PPLG. sebagai projek pembelajaran, sekaligus membantu
          teman-teman mendapatkan perlengkapan sekolah dengan mudah dan
          harga terjangkau.
        </p>

        <p>
          Setiap produk dipilih dan dikelola oleh tim kecil siswa dengan
          pengalaman langsung di bidang teknologi.
        </p>
      </div>

      <!-- Gambar di sebelah kanan -->
      <div class="GambarCerita">
        <img src="/image/topi.jpg" alt="Gambar Cerita" />
      </div>
    </div>

    <!-- Tim Kami -->
    <section class="Tim">
      <h1>Tim Kami</h1>

      <div class="DaftarTim">
        <div class="KartuTim">
          <div class="Avatar">A</div>
          <h3>Ahmad</h3>
          <p>Ketua Tim    </p>
        </div>

        <div class="KartuTim">
          <div class="Avatar">S</div>
          <h3>nono</h3>
          <p>Desainer UI</p>
        </div>

        <div class="KartuTim">
          <div class="Avatar">R</div>
          <h3>agus</h3>
          <p>Programmer</p>
        </div>
      </div>
    </section>
  </main>
</template>

<style>
/* =========================
   JUDUL
========================= */

.Judul {
  text-align: center;
  padding: 40px;
  background: linear-gradient(90deg, #263d8f, #3f51d1);
  color: white;
}

.Judul h1 {
  margin: 0;
}


/* =========================
   CERITA KAMI
========================= */

.Cerita {
  display: flex;
  align-items: center;
  justify-content: space-between;

  max-width: 900px;
  margin: 10px auto;
  padding: 0 40px;

  gap: 40px;
  background:whitesmoke;    
}

.IsiCerita {
  flex: 1;
}

.IsiCerita h1 {
  margin-bottom: 20px;
}

.IsiCerita p {
  line-height: 1.6;
  margin-bottom: 15px;
}


/* =========================
   GAMBAR
========================= */

.GambarCerita {
  flex: 1;
  display: flex;
  justify-content: center;
}

.GambarCerita img {
  width: 350px;
  height: 200px;

  object-fit: cover;
  border-radius: 15px;
}


/* =========================
   TIM KAMI
========================= */

.Tim {
  max-width: 900px;
  margin: 60px auto 0;
  padding: 50px 40px;

  background-color: #f5f9ff;
  text-align: center;
}

.Tim h1 {
  margin-bottom: 35px;
}

.DaftarTim {
  display: flex;
  justify-content: center;
  gap: 10px;
}

.KartuTim {
  width: 150px;
  padding: 20px;
  background-color: white;
  border-radius: 10px;

  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.Avatar {
  width: 50px;
  height: 50px;

  margin: 0 auto 10px;

  display: flex;
  align-items: center;
  justify-content: center;

  border-radius: 50%;

  background-color: #4438d8;
  color: white;

  font-size: 20px;
  font-weight: bold;
}

.KartuTim h3 {
  margin: 5px 0;
}

.KartuTim p {
  margin: 0;
  color: #777;
}
</style>