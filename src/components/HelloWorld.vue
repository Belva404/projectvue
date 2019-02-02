<template>
  <div class="hello">
    <h1 v-if="show">(◕ω◕)</h1>
    <h1 v-else>༼ಢ_ಢ༽</h1>

    <p v-if="nama">{{ nama }}</p>

    <input type="text" v-model="nama">

    <button type="button" v-on:click="hideTitle">OwO</button>
    <br>
    <h3>Jawaban benar : {{skor}}</h3>
    <li v-for="soal1 in soal1">
      <h3>{{soal1}}</h3>
      <jawaban1 v-for="jawaban1 in jawaban1">
        <br>
        <input type="radio" v-on:click="increment" value="A. Asep Tapip">
        {{jawaban1}}
      </jawaban1>
      <jawaban2 v-for="jawaban2 in jawaban2">
        <br>
        <input type="radio" v-on:click="increment" value="B. Kusmoro Rusli">
        {{jawaban2}}
      </jawaban2>
      <jawaban3 v-for="jawaban3 in jawaban3">
        <br>
        <input type="radio" v-on:click="increment" value="C. Belva Naufal Nugraha">
        {{jawaban3}}
      </jawaban3>
    </li>
    <br>
    <li v-for="soal2 in soal2">
      <h3>{{soal2}}</h3>
      <jawaban4 v-for="jawaban4 in jawaban4">
        <br>
        <input type="radio" v-on:click="increment" value="A. Selfie">
        {{jawaban4}}
      </jawaban4>
      <jawaban5 v-for="jawaban5 in jawaban5">
        <br>
        <input type="radio" v-on:click="increment" value="B. Sansss Lur, bumi cuma lagi goyang hehe">
        {{jawaban5}}
      </jawaban5>
      <jawaban6 v-for="jawaban6 in jawaban6">
        <br>
        <input type="radio" v-on:click="increment" value="C. Lari keluar rumah atau mencari lahan terbuka">
        {{jawaban6}}
      </jawaban6>
    </li>
    <br>
    <li v-for="soal3 in soal3">
      <h3>{{soal3}}</h3>
      <jawaban7 v-for="jawaban7 in jawaban7">
        <br>
        <input type="radio" v-on:click="increment" value="A. Mail">
        {{jawaban7}}
      </jawaban7>
      <jawaban8 v-for="jawaban8 in jawaban8">
        <br>
        <input type="radio" v-on:click="increment" value="B. Buku">
        {{jawaban8}}
      </jawaban8>
      <jawaban9 v-for="jawaban9 in jawaban9">
        <br>
        <input type="radio" v-on:click="increment" value="C. Hal hal imut">
        {{jawaban9}}
      </jawaban9>
    </li>
  </div>
  
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: function() {
    return {
      nama: 'Belva',
      show: 'true',
      skor: 0,
      soal1  : ['1. Siapa Kepala Sekolah SMKN 4 Negeri Bandung'],
      jawaban1 : ['A. Asep Tapip'],
      jawaban2 : ['B. Kusmoro Rusli'],
      jawaban3 : ['C. Belva Naufal Nugraha'],      
      soal2  : ['2. Apa yang harus dilakukan ketika terjadi gempa'],
      jawaban4 : ['A. Selfie'],
      jawaban5 : ['B. Sansss Lur, bumi cuma lagi goyang hehe'],
      jawaban6 : ['C. Lari keluar rumah atau mencari lahan terbuka'],
      soal3  : ['3. Apa yang tidak disukai Mei Mei'],
      jawaban7 : ['A. Mail'],
      jawaban8 : ['B. Buku'],
      jawaban9 : ['C. Hal hal imut'],
    }
  },
  methods: {
    hideTitle () {
      this.show = !this.show
    },
    increment () {
      var value = event.target.value;
      if (value === "A. Asep Tapip"){
        this.skor++;
      }else if (value === "C. Lari keluar rumah atau mencari lahan terbuka"){
        this.skor++;
      }else if (value === "A. Mail"){
        this.skor++;
      }else{
        this.skor--;
      }
    }
  },
  mounted: function() {
    this.nama = "Duivel"
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

h1{
  color: #42b983;
}

p{
  color: #42b983;
}
</style>
<style>
body{
  background-color: black;
}
</style>

