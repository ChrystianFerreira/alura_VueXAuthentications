<template>
  <div>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item">
            <router-link class="nav-link" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/gerentes" class="nav-link">
              Gerentes
            </router-link>
          </li>
          <li class="nav-item">
            <a
             class="nav-link"
              href="#"
              @click.prevent="efetuarLogout">Logout</a>
          </li>
        </ul>
      </div>
  </div>
</template>

<script>
import { logoutMixin } from '@/mixins'

export default {
  mixins: [ logoutMixin ]  
}
</script>

<style>

</style>