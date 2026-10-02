<script setup>
import { ref } from 'vue'

const faqAktif = ref(null)

const faqs = [
  {
    pertanyaan: 'Apa itu OnlineShop Sekolah?',
    jawaban: 'OnlineShop Sekolah adalah website untuk melihat dan membeli produk yang tersedia di sekolah.'
  },
  {
    pertanyaan: 'Bagaimana cara membeli produk?',
    jawaban: 'Pilih produk yang kamu inginkan, masukkan ke keranjang, kemudian lanjutkan ke proses pembelian.'
  },
  {
    pertanyaan: 'Bagaimana cara melihat produk yang tersedia?',
    jawaban: 'Kamu dapat melihat produk yang tersedia melalui halaman Product.'
  },
  {
    pertanyaan: 'Bagaimana cara menghubungi kami?',
    jawaban: 'Kamu dapat menghubungi kami melalui halaman Contact.'
  },
  {
    pertanyaan: 'Apakah produk selalu tersedia?',
    jawaban: 'Ketersediaan produk dapat berubah sesuai dengan stok yang tersedia.'
  }
]

function bukaFAQ(index) {
  if (faqAktif.value === index) {
    faqAktif.value = null
  } else {
    faqAktif.value = index
  }
}
</script>


<template>
  <main class="faq-page">

    <div class="faq-header">
      <div class="icon">?</div>

      <h1>Frequently Asked Questions</h1>

      <p>
        Temukan jawaban dari pertanyaan yang sering ditanyakan
        mengenai OnlineShop Sekolah.
      </p>
    </div>


    <div class="faq-container">

      <div
        v-for="(faq, index) in faqs"
        :key="index"
        class="faq-item"
        :class="{ aktif: faqAktif === index }"
      >

        <button
          class="faq-question"
          @click="bukaFAQ(index)"
        >
          <span>{{ faq.pertanyaan }}</span>

          <span class="arrow">
            {{ faqAktif === index ? '−' : '+' }}
          </span>
        </button>


        <div
          v-if="faqAktif === index"
          class="faq-answer"
        >
          <p>{{ faq.jawaban }}</p>
        </div>

      </div>

    </div>


    <div class="faq-footer">

      <h2>Masih punya pertanyaan?</h2>

      <p>
        Jangan ragu untuk menghubungi kami jika membutuhkan
        informasi lebih lanjut.
      </p>

      <router-link
        to="/Contact"
        class="contact-button"
      >
        Hubungi Kami
      </router-link>

    </div>

  </main>
</template>


<style scoped>

.faq-page {
  min-height: 100vh;
  padding: 50px 20px;
  box-sizing: border-box;

  background: linear-gradient(
    135deg,
    #eef5ff,
    #f8f4ff
  );
}


/* HEADER */

.faq-header {
  text-align: center;
  max-width: 700px;
  margin: 0 auto 40px;
}

.icon {
  width: 65px;
  height: 65px;
  margin: 0 auto 15px;

  display: flex;
  justify-content: center;
  align-items: center;

  border-radius: 50%;

  background: linear-gradient(
    135deg,
    #2563eb,
    #7c3aed
  );

  color: white;

  font-size: 32px;
  font-weight: bold;

  box-shadow: 0 8px 20px rgba(37, 99, 235, 0.25);
}

.faq-header h1 {
  margin: 0;

  font-size: 36px;

  background: linear-gradient(
    90deg,
    #2563eb,
    #7c3aed
  );

    color:white;
}

.faq-header p {
  margin-top: 12px;

  color: #64748b;

  font-size: 16px;

  line-height: 1.6;
}


/* FAQ */

.faq-container {
  max-width: 800px;
  margin: auto;
}

.faq-item {
  margin-bottom: 14px;

  background: white;

  border: 2px solid transparent;
  border-radius: 12px;

  overflow: hidden;

  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);

  transition: all 0.25s ease;
}

.faq-item:hover {
  transform: translateY(-2px);

  border-color: #93c5fd;

  box-shadow:
    0 8px 20px rgba(37, 99, 235, 0.12);
}

.faq-item.aktif {
  border-color: #6366f1;
}


/* QUESTION */

.faq-question {
  width: 100%;

  padding: 20px;

  display: flex;
  justify-content: space-between;
  align-items: center;

  background: white;

  border: none;

  cursor: pointer;

  text-align: left;

  color: #1e293b;

  font-size: 16px;
  font-weight: 600;
}

.faq-question:hover {
  color: #2563eb;
}


/* + / - */

.arrow {
  min-width: 32px;
  height: 32px;

  display: flex;
  justify-content: center;
  align-items: center;

  border-radius: 50%;

  background: #eff6ff;

  color: #2563eb;

  font-size: 22px;
}

.faq-item.aktif .arrow {
  background: linear-gradient(
    135deg,
    #2563eb,
    #7c3aed
  );

  color: white;
}


/* ANSWER */

.faq-answer {
  padding: 0 20px 20px;

  color: #64748b;

  line-height: 1.7;
}

.faq-answer p {
  margin: 0;

  border-left: 3px solid #6366f1;

  padding-left: 15px;
}


/* FOOTER */

.faq-footer {
  max-width: 800px;

  margin: 45px auto 0;

  padding: 35px;

  text-align: center;

  background: linear-gradient(
    135deg,
    #2563eb,
    #7c3aed
  );

  color: white;

  border-radius: 15px;

  box-shadow:
    0 10px 25px rgba(37, 99, 235, 0.2);
}

.faq-footer h2 {
  margin-top: 0;
}

.faq-footer p {
  color: #e0e7ff;
}


/* BUTTON */

.contact-button {
  display: inline-block;

  padding: 11px 22px;

  background: white;

  color: #2563eb;

  text-decoration: none;

  border-radius: 8px;

  font-weight: 600;
}

.contact-button:hover {
  transform: translateY(-2px);
}

</style>