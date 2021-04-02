<template>
  <div class="container">
    <h1>Novo usuário</h1>
    <form @submit.prevent="enviarFormulario">
      <div class="form-roup">
        <label for="nome">Nome</label>
        <input v-model="usuario.nome" type="text" class="form-control" />
      </div>
      <div class="form-roup">
        <label for="nome">E-Mail</label>
        <input v-model="usuario.email" type="email" class="form-control" />
      </div>
      <div class="form-roup">
        <label for="nome">Senha</label>
        <input v-model="usuario.senha" type="password" class="form-control" />
      </div>
      <button class="btn btn-primary" type="submit">Salvar</button>
    </form>
  </div>
</template>

<script>

export default {
  
  data() {
    return {
      usuario: {
        nome: '',
        senha: '',
        email: ''
      }
    }
  },
  methods: {
    enviarFormulario() {
      this.$http.post('auth/register', this.usuario)
        .then(response => {
          console.log(response)
          this.$router.push({name: 'login'})
        })
        .catch(error => console.log(error))
    }
  }

}
</script>

<style>

</style>