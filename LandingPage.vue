<template>
    <main>
        <div class="Card1">
            <h1>Belanja perlengkapan sekolah, gampang & terpercaya</h1>
            <p>Mulai dari kaos,topi,sampai tas sekolah - semua ada di satu  tempat</p>
        <button><RouterLink to="/product">Lebih lengkap</RouterLink></button>
    </div>
    <div class="Container">
        <div class="Card">
            <p>🛡️</p>
            <h2>Kualitas Terjamin</h2>
            <p>Bahan dipilih oleh ahli sekolah</p>
        </div>
        <div class="Card">
            <p>✅</p>
            <h2>Harga bersahabat</h2>
            <p>Harga murah dikalangan siswa</p>
        </div>
        <div class="Card">
            <p>⚡</p>
            <h2>Penjualan Terlaris</h2>
            <p>Produk paling laris di toko kami</p>
            </div>
        </div>
    </main>
    </template>
    <style scoped>
.Card1{
        text-align: center;
        padding: 70px;
        background: linear-gradient(90deg, #1a38a1, #3f51d1);
        color:rgb(204, 48, 48);
        align-items: center;
        box-shadow: 20%;
        border-radius: 10px;
}
.Card{
        text-align: center;
        padding: 16px;  
        border-radius: 10px;
        border: 1px;
        width: 175px;  
        margin-top: 20px;
        margin-left: 10px;
        background: linear-gradient(90deg, #263d8f, #3f51d1);
        color:rgb(112, 30, 219);
        box-shadow: 20%;
        justify-content: space-between;
}
.Container{
        display: flex;
        justify-content: center;
        align-items: center;
        box-shadow: 20%;
        align-items: center;
        background:whitesmoke;
        margin-top: 20px;
}
</style>