<template>
  <div class="about">
    <div class="heading">
      <h1>Play Sound</h1>
      <h4>Playing audio files with Vue.js</h4>
    </div>
    <div class="botonario">
      <div class="form-group">
        <label>
          <button class="btn btn-primary btn-sm" 
            @click.prevent="reproducirsonido('http://soundbible.com/mp3/Air Plane Ding-SoundBible.com-496729130.mp3', 1)">
          </button>
          Play Air Plane Ding
        </label>
        <br>
        <label>
          <button class="btn btn-primary btn-sm" 
            @click.prevent="reproducirsonido('http://soundbible.com/mp3/Elevator Ding-SoundBible.com-685385892.mp3', 0)">
          </button>
          Play Elevator Ding
        </label>
  </div>
    </div>
  </div>
</template>

<style scoped>
.about{
  background-color: rgb(0, 119, 255);
  height: 50%;
}

.heading h1 {
  background: -webkit-linear-gradient(#fff, #999);
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
  text-align: center;
  margin: 0 0 5px 0;
  font-weight: 900;
  font-size: 4rem;
  color: #fff;
}

.heading h4 {
  color: #90b4cc;
  text-align: center;
  margin: 0 0 35px 0;
  font-weight: 400;
  font-size: 24px;
}

.botonario {
  padding: 40px 80px 15px 80px;
  background-color: #fff;
  border-radius: 8px;
  max-width: 400px;
}

.btn {
  outline: none !important;
}

.btn.btn-primary {
  background-color: #5c4084;
  border-color: #5c4084;
  outline: none;
}
.btn.btn-primary:hover {
  background-color: #442f62;
  border-color: #442f62;
}
.btn.btn-primary:active, .btn.btn-primary:focus {
  background-color: #684895;
  border-color: #684895;
}
.btn.btn-primary .fa {
  padding-right: 4px;
}

.btn-sm {
  font-size: 22px;
  padding: 2px 1px 2px 4px;
  line-height: 12px;
  margin-right: 10px;
}

.form-group {
  margin-bottom: 25px;
}
</style>

<script>
export default {
  name: 'audio',
  methods:{
    reproducirsonido (sonido, ventana){
      if(sonido){
        var sonido1 = new Audio(sonido)
        sonido1.play()

        if(ventana == 1){
          alert("soylaventana")
        }
      }
    }
  }
}
</script>