<template>
  <div class="hello">
    <h1 v-if="show">{{ msg }}</h1>
    <h1 v-else>Judul Disembunyikan</h1>
    <p>Skor : {{skor}}/3</p>
    <p>{{ nama}}</p>
    <input type="text" v-model="nama">
    <button type="button" v-on:click="hideTitle">Click Me</button>
    <br>
    <!--SOAL1-->
    <li v-for="s in soal">
    <h3>{{s}}</h3>
    <jawaban1 v-for="j in jawaban1">
    <br>
    <input type="radio" v-on:click="increment" value="A.Adam">
    {{j}}
    </jawaban1>
    <br>
    <jawaban2 v-for="a in jawaban2">
    <input type="radio" v-on:click="increment" value="B.Joni">
    {{a}}
    </jawaban2>
    <br>
    <jawaban3 v-for="w in jawaban3">
    <input type="radio" v-on:click="increment" value="C.Kesbor">
    {{w}}
    </jawaban3>
    <br>
    <jawaban4 v-for="b in jawaban4">
    <input type="radio" v-on:click="increment" value="D.Marcus">
    {{b}}
    </jawaban4>
    <!--SOAL2-->
      <li v-for="o in soal2">
    <h3>{{o}}</h3>
    <option1 v-for="p in option1">
    <br>
    <input type="radio" v-on:click="increment" value="A.tepat">
    {{p}}
    </option1>
    <br>
    <option2 v-for="t in option2">
    <input type="radio" v-on:click="increment" value="B.yang paling tepat">
    {{t}}
    </option2>
    <br>
    <option3 v-for="i in option3">
    <input type="radio" v-on:click="increment" value="C.paling tepat">
    {{i}}
    </option3>
    <br>
    <option4 v-for="n in option4">
    <input type="radio" v-on:click="increment" value="D.benar">
    {{n}}
    </option4>
     <!--SOAL3-->
      <li v-for="l in soal3">
    <h3>{{l}}</h3>
    <choose1 v-for="c in choose1">
    <br>
    <input type="radio" v-on:click="increment" value="A.Vikendi">
    {{c}}
    </choose1>
    <br>
    <choose2 v-for="e in choose2">
    <input type="radio" v-on:click="increment" value="B.Sanhok">
    {{e}}
    </choose2>
    <br>
    <choose3 v-for="s in choose3">
    <input type="radio" v-on:click="increment" value="C.DUST II">
    {{s}}
    </choose3>
    <br>
    <choose4 v-for="h in choose4">
    <input type="radio" v-on:click="increment" value="D.Erangel">
    {{h}}
    </choose4>
    </li>
  </div>
</template>
<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data : function() {
  return{
    nama: 'Farhan',
    show: true,
    skor: 0,
    soal : ['1.Siapakah Manusia Pertama di Bumi?'],
    jawaban1 : ['A.Adam'],
    jawaban2 : ['B.Joni'],
    jawaban3 : ['C.Kesbor'],
    jawaban4 : ['D.Marcus'],
    soal2 : ['2.Mana jawaban yang paling tepat?'],
    option1 : ['A.tepat'],
    option2 : ['B.yang paling tepat'],
    option3 : ['C.paling tepat'],
    option4 : ['D.benar'],
    soal3 : ['3.Dibawah ini adalah map PUBG, kecuali'],
    choose1 : ['A.Vikendi'],
    choose2 : ['B.Sanhok'],
    choose3 : ['C.DUST II'],
    choose4 : ['D.Erangel']
    }
    },
  methods: {
    hideTitle() {
      this.show = !this.show
    },
    increment() {
    var value = event.target.value;
    if (value === "A.Adam"){
    this.skor++;
    }else if (value === "B.yang paling tepat"){
    this.skor++;
    }else if (value === "C.DUST II"){
    this.skor++;
    }else{
			this.skor--;
		}
    }
  },
  mounted: function () {
    this.nama = 'Farhan'
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
</style>
