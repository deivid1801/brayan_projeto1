<script setup>
import { ref } from 'vue'

const email = ref('')
const nome = ref('')
const dataN = ref('')
const endereço = ref('')
const cidade = ref('')
const estado = ref('')
const Hobbies = ref('')
const Linguagens = ref('')
const Biografia = ref('')
const senha = ref('')
const confirmaçao = ref('')
const botaoDados = ref('')
function limpardados (){
  email.value = ""
  nome.value = ""
  dataN.value = ""
  endereço.value = ""
  cidade.value = ""
  estado.value = ""
  Hobbies.value = ""
  Linguagens.value = ""
  Biografia.value = ""
  senha.value = ""
  confirmaçao.value = ""
  botaoDados.value = false
}




</script>

<template>
  <form class="edit">
  <div class="row">
    <div class="col">
      <input type="text" v-bind:value="email" v-on:input="event => email = event.target.value" class="form-control"
          placeholder="Enter email" name="email ">
        <input type="text" v-bind:value="nome" v-on:input="event => nome = event.target.value" class="form-control"
          placeholder="insira seu nome">
        <input type="text" v-bind:value="dataN" v-on:input="event => dataN = event.target.value" class="form-control"
          placeholder="insira sua data de nascimento">
        <input type="text" v-bind:value="endereço" v-on:input="event => endereço = event.target.value"
          class="form-control" placeholder="insira seu endereço">
        <input type="text" v-bind:value="cidade" v-on:input="event => cidade = event.target.value" class="form-control"
          placeholder="insira sua cidade">
     

      <p><h6>insira seu Estado</h6>  </p>

     <select v-bind:value="estado" v-on:input="event => estado = event.target.value" class="form-select mt-3">
     <option>AC</option>
     <option>AL</option>
     <option>AP</option>
     <option>AM</option>
     <option>BA</option>
     <option>CE</option>
     <option>DF</option>
     <option>ES</option>
     <option>GO</option>
     <option>MA</option>
     <option>MT</option>
     <option>MS</option>
     <option>MG</option>
     <option>PA</option>
     <option>PB</option>
     <option>PR</option>
     <option>PE</option>
     <option>PI</option>
     <option>RJ</option>
     <option>RN</option>
     <option>RS</option>
     <option>RO</option>
     <option>RR</option>
     <option>SC</option>
     <option>SP</option>
     <option>SE</option>
     <option>TO</option>
   </select>
   <input type="text" v-bind:value="Hobbies" v-on:input="event => Hobbies = event.target.value" class="form-control" placeholder="insira seus Hobbies
">
   <input type="text" v-bind:value="Linguagens" v-on:input="event => Linguagens = event.target.value" class="form-control" placeholder="insira suas Linguagens de programação
">
   <input type="text" v-bind:value="Biografia" v-on:input="event => Biografia = event.target.value" class="form-control" placeholder="insira sua Biografia">
   <input type="password" v-bind:value="senha" v-on:input="event => senha = event.target.value" class="form-control" placeholder="insira sua senha" name="pswd">
      <input type="password" v-bind:value="confirmaçao" v-on:input="event => 
      confirmaçao = event.target.value" class="form-control" placeholder="confirmaçao de senha" name="pswd">

    </div>
   
  </div>

</form>


<button v-on:click="botaoDados = true " class="bot1">mostrar dados do usuario</button>
<button @click="limpardados" class="bot2"> limpar dados</button>

<div v-if = "botaoDados" class="dados">
<h4>dados usuario</h4>
    <p>email digitado: {{ email }}</p>
<p>nome digitado:{{ nome }}</p>
<p>data de nascimento digitado:{{ dataN }}</p>
<p>endereço digitado:{{ endereço }}</p>
<p>cidade digitado:{{ cidade }}</p>
<p>estado digitado:{{ estado }}</p>
<p>Hobbies digitado:{{ Hobbies }}</p>
<p>Linguagens digitado:{{ Linguagens }}</p>
<p>biografia digitado:{{ Biografia }}</p>
<p>senha digitado:{{ senha }}</p>
<p>confirmaçao digitado:{{ confirmaçao }}</p>
</div>

</template>

<style scoped>
.edit{
 width: 1200px;
  height: 480px;
  margin-left: 200px;
  background-color: aqua;
}
.bot1{
  margin-left: 200px;
}
.dados{
  margin-left: 200px;
  background-color:aqua;
  margin-right: 130px;
}
.form-control{
  font: italic;
}
</style>
