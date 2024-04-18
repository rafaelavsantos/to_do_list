<template>
  <div class="todo-list">
    <form @submit.prevent="addTask()">
      <div class="input-container">
        <input type="text" name="activies" id="activies" placeholder="Adicione um novo item ...">
        <button type="submit">Adicionar</button>
      </div>
    </form>

      <div class="tasks">
        <div class="task">
          <div class="check">
            <Check v-if="showCheck" @click="checkTask()" class="icons" />
            <input type="text" name="activies" id="activies" placeholder="Task BD ..." />
          </div>
          <Trash2 @click="deleteTask()" class="icons" />
        </div>
      </div>
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
.todo-list {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 20px;
}

.input-container {
  display: flex;
  margin-bottom: 20px;
}

.input-container input[type="text"] {
  font-size: 1.2em;
  padding: 10px;
  border: none;
  border-left: 2px solid #359d5d;
  color: #BFC1CD;
  width: 400px;
}

.input-container input:focus {
  outline: none;
}

.input-container button {
  font-size: 1em;
  padding: 10px;
  border: none;
  color: #359d5d;
  font-weight: bold;
  text-transform: uppercase;
  cursor: pointer;
}

.task {
  padding: 10px;
  background-color: #BFC1CD;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.check {
  background-color: #BFC1CD;
  color: #359d5d;
  display: flex;
  align-items: center;
}

.check input {
  border: none;
  background-color: transparent;
  font-size: 1em;
  padding-left: 10px;
  width: 440px;
}

.check input:focus {
  outline: none;
}

.icons {
  background-color: transparent;
  cursor: pointer;
}
</style>
