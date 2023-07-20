<script setup>
let msg = "Hallo Dunia";
let headName = "<h1>Nama saya Al-farizy<h1>";
let seen = true;
let message = ref("Hai Vue JS");
function balikkanPesan(){
  message.value = message.value.split('').reverse().join('');
}

let todos=[
  {teks:'Belajar javascript'},
  {teks: 'belajar vue'},
  {teks: 'belajar proyek'}
]

let pesan = ref("hai vue");

</script>

<template>
  <div>
    <span>{{ msg }}</span><br>
    <span style="color: red;">Ini warna merah</span><br>
    <span v-html="headName"></span>

    <button :disabled="isButtonDisabled">Button</button>
    {{ number + 1 }}<br>
    {{ ok ? 'YES': 'NO'}}<br>
    {{ msg.split('').reverse().join('') }}

    <p v-if="seen">Now you see me</p>

    <div v-bind:id="'list-' + id"></div>

    <p v-if="seen">Sekarang Anda bisa melihatku</p>

    <a v-bind:href="url"> coy </a>
    
    <a v-on:click="doSomething"> say </a>

    <a v-bind:[namaAtribut]="url">hai </a>

    <a v-on:[namaEvent]="doSomething"> lose </a>

    <form v-on:submit.prevent="onSubmit">win</form>

   
 
  </div>
  <p>{{ message }}</p>
  <button v-on:click="balikkanPesan">Balikan psan</button>

  <br>pengulanngan
  <ol>
    <li v-for="todo in todos">
      {{ todo.teks }}

    </li>
  </ol>

  <p>{{ pesan }}</p>
  <input v-model="pesan">
</template>