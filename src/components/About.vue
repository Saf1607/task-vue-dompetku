<template>
    <div class="about">
      <div class="content">
        <h1>Tentang Kami</h1>
        <p>
          Dompetku adalah aplikasi pengelolaan keuangan pribadi yang dirancang untuk membantu Anda mencatat dan mengatur pengeluaran serta pemasukan dengan mudah dan efektif.
        </p>
  
        <div class="values">
          <div class="value-item">
            <h2>Misi Kami</h2>
            <p>
              Memberikan solusi yang sederhana dan efektif untuk pengelolaan keuangan pribadi, membantu pengguna memahami pola pengeluaran mereka, dan mendukung mereka dalam merencanakan masa depan finansial yang lebih baik.
            </p>
          </div>
          <div class="value-item">
            <h2>Visi Kami</h2>
            <p>
              Menciptakan generasi yang lebih melek finansial dan mampu mencapai tujuan finansial mereka, dengan memberikan akses ke alat yang membantu mereka mengelola uang secara efisien.
            </p>
          </div>
          <div class="value-item">
            <h2>Nilai Kami</h2>
            <p>
              Kami percaya pada transparansi, kejujuran, dan komitmen terhadap keberlanjutan finansial. Kami selalu berusaha untuk meningkatkan layanan kami agar dapat memberikan dampak positif bagi semua pengguna.
            </p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <style scoped>
  .about {
    padding: 2rem;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    background-color: #f9f9f9;
    color: #333;
    min-height: 100vh;
  }
  
  .content {
    max-width: 900px;
    padding: 1.5rem;
  }
  
  h1 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    color: #4CAF50;
  }
  
  p {
    font-size: 1.1rem;
    line-height: 1.7;
    margin-bottom: 1.5rem;
  }
  
  .values {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    margin-top: 2.5rem;
  }
  
  .value-item {
    padding: 2rem;
    background-color: #ffffff;
    border-radius: 12px;
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  .value-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
  }
  
  .value-item h2 {
    font-size: 1.6rem;
    color: #333;
    margin-bottom: 0.5rem;
  }
  
  .value-item p {
    font-size: 1rem;
    color: #555;
  }
  
  @media (min-width: 768px) {
    .values {
      flex-direction: row;
    }
  }
  
  @media (min-width: 1024px) {
    h1 {
      font-size: 3rem;
    }
  
    .value-item h2 {
      font-size: 1.8rem;
    }
  
    .value-item p {
      font-size: 1.1rem;
    }
  }
  </style>
  
  <script>
  export default {
    name: "About",
  };
  </script>
  