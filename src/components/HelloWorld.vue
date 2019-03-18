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
    <button type="button" v-on:click="hideTitle">Submit</button>
    </div>
    <div v-else>
      <h1>Nilai Akhir</h1>
      <h2>Benar : {{jumlah_benar() }}</h2>
      <h2>Salah : {{jumlah_salah() }}</h2>
      <h2>Nilai: {{ nilai() }}</h2>
    </div>
    </center>
  </div>
</template>

<script>
export default {
  name: 'Thoriq',
  data () {
    return {
      msg: 'Quiz',
      show:true,
      btnShow:true,
      picked1:'',picked2:'',picked3:'',picked4:'',picked5:'',
      soal1:[
      {
        no:'1',
        soal:"Nama tornado terbesar yang pernah terjadi di bumi adalah...",
        jaw_a:"A. Moore Tornado",
        jaw_b:"B. Joplin Tornado",
        jaw_c:"C. Oklahoma Tornado",
        jaw_d:"D. Tri State Tornado",
        jaw_e:"E. El Reno Tornado"
      }
      ],
      soal2:[
      {
        no:'2',
        soal:"Prize pool game terbesar dalam tournament E-Sport adalah...",
        jaw_a:"A. Fortnite",
        jaw_b:"B. Counter Strike : Global Offensive",
        jaw_c:"C. Player Unknown Battle Ground",
        jaw_d:"D. Dota 2",
        jaw_e:"E. League Of Legend"
      }
    ],
      soal3:[
      {
        no:'3',
        soal:"Search engine yang sering digunakan adalah...",
        jaw_a:"A. Google",
        jaw_b:"B. Bing",
        jaw_c:"C. Yahoo",
        jaw_d:"D. Baidu",
        jaw_e:"E. DuckDuckGo"
      }
    ],
      soal4:[
      {
        no:'4',
        soal:"Planet ke-5 dalam urutan tata surya adalah...",
        jaw_a:"A. Planet Bumi",
        jaw_b:"B. Planet Yupiter",
        jaw_c:"C. Planet Neptunus",
        jaw_d:"D. Planet Saturnus",
        jaw_e:"E. Planet Mars"
      }
    ],
      soal5:[
      {
        no:'5',
        soal:"Sim yang wajib dimiliki pengendara motor 250cc adalah...",
        jaw_a:"A. Sim A",
        jaw_b:"B. Sim B",
        jaw_c:"C. Sim C I",
        jaw_d:"D. Sim C II",
        jaw_e:"E. Sim C I & C II"
      }
    ]
    }
  },
  methods: {
    hideTitle () {
      this.show = !this.show
    },
    nilai: function(){
      var jaw_1, jaw_2, jaw_3, jaw_4, jaw_5;

      if(this.picked1 == 'e'){ jaw_1 = 20; }else{ jaw_1 = 0;}
      if(this.picked2 == 'd'){ jaw_2 = 20; }else{ jaw_2 = 0;}
      if(this.picked3 == 'a'){ jaw_3 = 20; }else{ jaw_3 = 0;}
      if(this.picked4 == 'b'){ jaw_4 = 20; }else{ jaw_4 = 0;}
      if(this.picked5 == 'e'){ jaw_5 = 20; }else{ jaw_5 = 0;}

      return jaw_1 + jaw_2 + jaw_3 + jaw_4 + jaw_5;

    },
    jumlah_benar: function(){
      return this.nilai() / 20;
    },
    jumlah_salah: function(){
      return 5 - this.jumlah_benar() ;
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
