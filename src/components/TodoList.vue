<template>
  <div class="container">
    <form>
      <div class="container-form">
        <input type="text" name="activies" id="activies" placeholder="Adicione um novo item ...">
        <button>Adicionar</button>
      </div>

      <div class="container-task">
        <div class="container-res">
          <img v-if="showCheck" @click="checkTask()" src="../assets/check-grey.png" alt="Botão de check da atividade">
          <img v-else @click="checkTask()" src="../assets/check-green.png" alt="Botão de check da atividade">
          <input type="text" name="activies" id="activies" placeholder="Adicione um novo item ..." />
        </div>
        <img class="delete" src="../assets/delete.png" alt="Botão de deletar" @click="deleteTask()">
      </div>

    </form>
  </div>
</template>

<script>
import { api } from '@/boot/axios';

export default {
  name: 'TodoList',
  data() {
    return {
      showCheck: true,
    }
  }, 
  methods: {
    checkTask() {
      this.showCheck = !this.showCheck;
    },
    deleteTask() {
      // conexão do back e front feita
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap');

* {
  font-family: "Open Sans", sans-serif;
}

.container {
  display: flex;
  justify-content: center;
}

.container-form {
  display: flex;
  align-items: center;
  width: 500px;
  margin-top: 20px;
  padding: 10px;
  background-color: #0A0D14;
  border-left: 2px solid #296F44;
}

.container-form input {
  border: none;
  width: 100%;
  font-size: 16px;
  background-color: transparent;
}

.container-form input:focus {
  outline: none;
}

.container-form button {
  border: none;
  text-transform: uppercase;
  color: #359d5d;
  font-weight: bold;
  background-color: transparent;
  cursor: pointer;
}

.container-task {
  background-color: #BFC1CD;
  padding: 10px;
  margin-top: 10px;
  display: flex;
  justify-content: space-between;

}

.container-task img {
  width: 20px;
  background-color: transparent;
  cursor: pointer;
}

.container-res {
  background-color: transparent;
  width: 100%;
}

.container-res input {
  background-color: transparent;
  color: #0A0D14;
  border: none;
  width: 85%;
  padding-left: 10px;
}

.container-res input:focus {
  outline: none
}

.container-res  {
  cursor: pointer;
}
</style>
