<template>
    <div class="dompetku">
      <h1>Dompetku</h1>
      <h2>Expense & Income Money Management</h2>
      
      <!-- Form Input -->
      <form @submit.prevent="addRecord">
        <input v-model="description" placeholder="Keterangan" required />
        <input v-model.number="amount" type="number" placeholder="Jumlah Uang" required />
        <button type="submit">Submit</button>
      </form>
  
      <!-- List Data -->
      <ul>
        <li v-for="(record, index) in records" :key="index">
          <span>{{ record.description }} - Rp{{ record.amount.toLocaleString() }}</span>
          <button @click="deleteRecord(index)" class="delete-btn">Hapus</button>
        </li>
      </ul>
  
      <!-- Tombol Hapus Semua -->
      <button @click="clearAll" class="clear-all">Hapus Semua Data</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        description: '',
        amount: null,
        records: []
      };
    },
    methods: {
      addRecord() {
        // Tambah data baru ke list
        this.records.push({
          description: this.description,
          amount: this.amount
        });
        // Reset input
        this.description = '';
        this.amount = null;
      },
      deleteRecord(index) {
        // Hapus data pada index tertentu
        this.records.splice(index, 1);
      },
      clearAll() {
        // Hapus semua data
        this.records = [];
      }
    }
  };
  </script>
  
  <style scoped>


  /* .dompetku {
    padding: 2rem;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    background-color: #f9f9f9;
    color: #333;
  } */

  .dompetku {
    max-width: 500px;
    margin: 1em;
    padding: 1em;
    border: 1.5px solid #ddd;
    border-radius: 8px;
    text-align: center;
  }
  
  form {
    margin-bottom: 1em;
  }
  
  input {
    margin: 0.5em 0;
    padding: 0.5em;
    width: 100%;
    box-sizing: border-box;
  }
  
  button {
    margin-top: 0.5em;
    padding: 0.5em;
    width: 100%;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  li {
    margin: 0.5em 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0.5em;
    border: 1px solid #ddd;
    border-radius: 4px;
    background-color: #f9f9f9;
  }
  
  .delete-btn {
    padding: 0.3em 0.5em;
    background-color: #f44336;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 0.9rem;
    width: auto;
  }
  
  .clear-all {
    margin-top: 1em;
    background-color: #f44336;
    color: white;
    border: none;
    border-radius: 4px;
    padding: 0.7em 1em;
    cursor: pointer;
    font-size: 1rem;
  }
  
  .clear-all:hover, .delete-btn:hover {
    background-color: #d32f2f;
  }
  
  </style>
  