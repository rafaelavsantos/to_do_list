<template>
  <div class="container">
    <form>
      <div class="container-form">
        <input type="text" name="activies" id="activies" placeholder="Adicione um novo item ...">
        <input type="submit" value="Adicionar">
      </div>

      <div class="container-res">
        <div class="container-task">
          <div class="check">
            <Check v-if="showCheck" @click="checkTask()" class="icons" />
            <input type="text" name="activies" id="activies" placeholder="Task BD ..." />
          </div>
          <Trash2 @click="deleteTask()" class="icons" />
        </div>
      </div>
    </form>
  </div>
</template>

<script>
import { Check, Trash2 } from 'lucide-vue-next';

export default {
  name: 'TodoList',
  components: {
    Check,
    Trash2,
  },
  data() {
    return {
      showCheck: true,
    }
  },
  methods: {
    checkTask() {
      console.log("Clicou")
    },
    deleteTask() {
      // conexão do back e front feita
    }
  }
}
</script>

<style scoped>
/*
  cores:
  verde #296F44
  dark #0A0D14
  cinza: #BFC1CD
  verde claro: #359d5d

*/

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

form {
  max-width: 500px;
  margin-top: 20px;
}


.container-form>#activies {
  font-size: 1.2em;
  padding: 10px;
  border: none;
  border-left: 2px solid #359d5d;
}

.container-form>#activies:focus {
  outline: none;
}

.container-form>input[type="submit"] {
  font-size: 1em;
  padding: 10px;
  border: none;
  color: #359d5d;
  font-weight: bold;
  text-transform: uppercase;
  cursor: pointer;
}

.container-task {
  margin-top: 20px;
  padding: 10px;
  background-color: aliceblue;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.check {
  background-color: aliceblue;
  color: #359d5d;
  display: flex;
  align-items: center;
}

.check input {
  border: none;
  background-color: transparent;
  padding-left: 10px;
}

.check input:focus {
  outline: none;
}

.icons {
  background-color: transparent;
  cursor: pointer;
}
</style>
