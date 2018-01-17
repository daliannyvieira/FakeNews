<template>
  <section class="comentarios">
    <h2 class="comentarios-titulo">Comentários</h2>
    <input class="comentarios-input" 
      v-model="novoComentario"
      placeholder='Digite seu comentário'
      v-on:keyup.enter="comentar">
    <button class="comentarios-button" v-on:click="comentar">Enviar</button>
    <ul>
      <li class='comentario' v-for='usuario in usuarios'>
        <img class='comentario-avatar' src='../assets/profile.svg'/>
        <div class='comentario-container'>
          <h3 class='comentario-titulo'>{{usuario.nome}}</h3>
          <p class='comentario-texto'>{{usuario.mensagem}}</p>
        </div>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: 'Comentarios',
  data () {
    return {
      novoComentario: '',
      usuarios: [
        {
          mensagem: 'Eu teria feito o mesmo sinceramente. Papai Noel nunca me deu oq eu pedi',
          nome: 'Camila RJ',
          imagem: '../assets/profile.svg'
        },
        {
          mensagem: 'kkkkkkkkkkkkkkkkkkkk rindo até 2049. Muito engraçado!!!!!',
          nome: 'Joaquim Campinas',
          imagem: '../assets/profile.svg'
        }
      ]
    }
  },
  methods: {
    comentar() {
      const comentario = {
        mensagem: this.novoComentario,
        nome: 'Visitante',
        imagem: this.usuarios.imagem
      }
      this.usuarios.push(comentario)
      this.novoComentario = ''
    }
  }
}
</script>

<style scoped>
.comentarios {
  padding: 0.75rem;
}
.comentarios-titulo {
  border-bottom: 1px solid black;
}
.comentarios-input {
  background-color: #fff;
  color: #E4E4E4;
  font-weight: bold;
  border: 0;
  border-bottom: 1px solid #E4E4E4;
  padding: 0.5rem;
  margin-right: 0.25rem;
  max-width: 70%;
}
.comentarios-button {
  color: #E4E4E4;
  background-color: #fff;
  font-weight: bold;
  border: 1px solid #E4E4E4;
  padding: 0.5rem;
}
.comentario {
  display: flex;
}
.comentario-container{
  display: flex;
  flex-direction: column;
  padding: 1rem 0;
}
.comentario-avatar {
  max-width: 70px;
  padding-right: 0.75rem;
}
.comentario-titulo {
  font-weight: bold;
  margin: 0;
  font-size: 11px;
}
.comentario-texto {
  margin: 0.25rem 0;
  font-weight: bold;
  color: #979797;
  font-size: 11px;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
