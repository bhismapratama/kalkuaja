<script>
export default {
  data() {
    return {
      nomorBang: 0,
      lanjut: 0,
      hasil: 0
    }
  },
  methods: {
    tambah() {
      this.hasil = this.nomorBang + this.lanjut;
    },  
    kurang() {
      this.hasil = this.nomorBang - this.lanjut;
    },
    kali() {
      this.hasil = this.nomorBang * this.lanjut;
    },
    bagi() {
      this.hasil = this.nomorBang / this.lanjut;
    },
  }
}
</script>

<template>
  <main>
    <header>
      <h1>kalku vue</h1>
    </header>
      <form @submit.prevent="">
        <label for="nom">nomor awal: </label>
        <input v-model="nomorBang" type="number" />
        <br />
        <label>lanjut: </label>
        <input v-model="lanjut" type="number" />
        <br />
        <label for="operasi">operasi: </label>
        <button @click="tambah()">tambah</button>
        <button @click="kurang()">kurang</button>
        <button @click="kali()">kali</button>
        <button @click="bagi()">bagi</button>
      </form>
      <p>Hasil perhitungan = {{ hasil }}</p>
  </main>
</template>
