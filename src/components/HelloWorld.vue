<template>
  <div class="hello">
  <center>
  <div v-if="show">
  <table><center><h1>Quiz</h1></center><hr><br>
    <div class="soal1" v-for="soal in soal1" v-bind:key="soal.soal1">
      <tr>
           <td><b>{{ soal.no }}.</b> {{ soal.soal }}</td> 
      </tr>
      <tr>
        <div class="Divide">
            <td>
              <input type="radio" name="soal1" value="a" v-model="picked1">{{soal.jaw_a}}
              <input type="radio" name="soal1" value="b" v-model="picked1">{{soal.jaw_b}}
              <input type="radio" name="soal1" value="c" v-model="picked1">{{soal.jaw_c}}
              <input type="radio" name="soal1" value="d" v-model="picked1">{{soal.jaw_d}}
              <input type="radio" name="soal1" value="e" v-model="picked1">{{soal.jaw_e}}
            </td>
        </div>
      </tr><br><hr>
    </div>
    <br>
    <div class="soal2" v-for="soal in soal2" v-bind:key="soal.soal2">
      <tr>
           <td><b>{{ soal.no }}.</b> {{ soal.soal }}</td>
      </tr>
      <tr>
        <div class="Divide">
            <td>
              <input type="radio" name="soal2" value="a" v-model="picked2">{{soal.jaw_a}}
              <input type="radio" name="soal2" value="b" v-model="picked2">{{soal.jaw_b}}
              <input type="radio" name="soal2" value="c" v-model="picked2">{{soal.jaw_c}}
              <input type="radio" name="soal2" value="d" v-model="picked2">{{soal.jaw_d}}
              <input type="radio" name="soal2" value="e" v-model="picked2">{{soal.jaw_e}}
            </td>
        </div>
      </tr><br><hr><br>
    </div>
    <div class="soal3" v-for="soal in soal3" v-bind:key="soal.soal3">
      <tr>
           <td><b>{{ soal.no }}.</b> {{ soal.soal }}</td>
      </tr>
      <tr>
        <div class="Divide">
            <td>
              <input type="radio" name="soal3" value="a" v-model="picked3">{{soal.jaw_a}}
              <input type="radio" name="soal3" value="b" v-model="picked3">{{soal.jaw_b}}
              <input type="radio" name="soal3" value="c" v-model="picked3">{{soal.jaw_c}}
              <input type="radio" name="soal3" value="d" v-model="picked3">{{soal.jaw_d}}
              <input type="radio" name="soal3" value="e" v-model="picked3">{{soal.jaw_e}}
            </td>
        </div>
      </tr><br><hr><br>
    </div>
     <div class="soal4" v-for="soal in soal4" v-bind:key="soal.soal4">
      <tr>
           <td><b>{{ soal.no }}.</b> {{ soal.soal }}</td>
      </tr>
      <tr>
        <div class="Divide">
            <td>
              <input type="radio" name="soal4" value="a" v-model="picked4">{{soal.jaw_a}}
              <input type="radio" name="soal4" value="b" v-model="picked4">{{soal.jaw_b}}
              <input type="radio" name="soal4" value="c" v-model="picked4">{{soal.jaw_c}}
              <input type="radio" name="soal4" value="d" v-model="picked4">{{soal.jaw_d}}
              <input type="radio" name="soal4" value="e" v-model="picked4">{{soal.jaw_e}}
            </td>
        </div>
      </tr><br><hr><br>
    </div>
    <div class="soal5" v-for="soal in soal5" v-bind:key="soal.soal5">
      <tr>
           <td><b>{{ soal.no }}.</b> {{ soal.soal }}</td>
      </tr>
      <tr>
        <div class="Divide">
            <td>
              <input type="radio" name="soal5" value="a" v-model="picked5">{{soal.jaw_a}}
              <input type="radio" name="soal5" value="b" v-model="picked5">{{soal.jaw_b}}
              <input type="radio" name="soal5" value="c" v-model="picked5">{{soal.jaw_c}}
              <input type="radio" name="soal5" value="d" v-model="picked5">{{soal.jaw_d}}
              <input type="radio" name="soal5" value="e" v-model="picked5">{{soal.jaw_e}}
            </td>
        </div>
      </tr><br><hr>
    </div>
    </table>
    </div>
    <div v-else>
      <h1>Hasil Akhir</h1>
      <h1>Nilai: {{ nilai() }}</h1>
      <h2>Jawaban benar : {{jumlah_benar() }}</h2>
      <h2>Jawaban salah : {{jumlah_salah() }}</h2>
    </div>
    <button v-if="btnShow" type="button" v-on:click="hideTitle">Submit</button>
    </center>
  </div>
</template>

<script>
export default {
  name: 'Gilby Faqih Hidayah Tauhid',
  data () {
    return {
      msg: 'Quiz',
      show:true,
      btnShow:true,
      picked1:'',picked2:'',picked3:'',picked4:'',picked5:'',
      soal1:[
      {
        no:'1',
        soal:"1*1 =",
        jaw_a:"A. 1111",
        jaw_b:"B. 111",
        jaw_c:"C. 11111",
        jaw_d:"D. 11",
        jaw_e:"E. 1"
      }
      ],
      soal2:[
      {
        no:'2',
        soal:"Kuda memiliki kaki sebanyak ?",
        jaw_a:"A. 30",
        jaw_b:"B. 4",
        jaw_c:"C. 15",
        jaw_d:"D. 2",
        jaw_e:"E. 6"
      }
    ],
      soal3:[
      {
        no:'3',
        soal:"ketika kita berada di bawah air laut, kita akan ?",
        jaw_a:"A. Tidak, karena memakai jas hujan",
        jaw_b:"B. Basah",
        jaw_c:"C. Tidur",
        jaw_d:"D. terbakar",
        jaw_e:"E. Terbang"
      }
    ],
      soal4:[
      {
        no:'4',
        soal:"Ibunya Jono mempunyai 5 anak,awa,iwi uwu ,dan owo .Nama anak kelimanya adalah ? ",
        jaw_a:"A. Tidak tahu karena tidak kenal",
        jaw_b:"B. sukardi",
        jaw_c:"C. surya",
        jaw_d:"D. Jono",
        jaw_e:"E. Ria"
      }
    ],
      soal5:[
      {
        no:'5',
        soal:"Hujan di bumi akan mengakibatkan banjir karena ?",
        jaw_a:"A. Tidak ada saluran perairan yang lancar",
        jaw_b:"B. Api",
        jaw_c:"C. Udara",
        jaw_d:"D. Batu",
        jaw_e:"E. Air"
      }
    ]
    }
  },
  methods: {
    nilai: function(){
      var jaw_1, jaw_2, jaw_3, jaw_4, jaw_5;

      if(this.picked1 == 'e'){ jaw_1 = 20; }else{ jaw_1 = 0;}
      if(this.picked2 == 'b'){ jaw_2 = 20; }else{ jaw_2 = 0;}
      if(this.picked3 == 'b'){ jaw_3 = 20; }else{ jaw_3 = 0;}
      if(this.picked4 == 'd'){ jaw_4 = 20; }else{ jaw_4 = 0;}
      if(this.picked5 == 'a'){ jaw_5 = 20; }else{ jaw_5 = 0;}

      return jaw_1 + jaw_2 + jaw_3 + jaw_4 + jaw_5;

    },
    jumlah_benar: function(){
      return this.nilai() / 20;
    },
    jumlah_salah: function(){
      return 5 - this.jumlah_benar() ;
    },
    hideTitle (){
    this.show = !this.show
    },
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
button {
  background-color: lightgray;
  border-radius: 8px;
  border-color: darkgray;
  padding: 5px;
  padding-right: 15px; 
  padding-left: 15px;
  margin: 15px; 
}
table {
  font-family: Times New Roman;
}
hr {
  border-style: groove;
  height: 2px;
  width: 156.9%;
  margin-left: -246px;
}
</style>
