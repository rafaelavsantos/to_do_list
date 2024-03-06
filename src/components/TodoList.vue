<template>
  <div class="container">
    <form>
      <input type="text" name="activies" id="activies" placeholder="Adicione um novo item ...">
      <button>Adicionar</button>
    </form>

    <div class="activies">
      <div class="ajustar-imagem">
        <img src="../assets/check-grey.png" alt="">
        <p>Estudar Vue 2 </p>
      </div>
      <img class="delete" src="../assets/delete.png" alt="">
    </div>

    <div class="activies">
      <div class="ajustar-imagem">
        <img src="../assets/check-green.png" alt="">
        <p>Estudar Vue 3 </p>
      </div>
      <img class="delete" src="../assets/delete.png" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: 'TodoList',

}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap');

* {
  margin: 0 auto;
  font-family: "Open Sans", sans-serif;
}

.container form {
  background-color: #0A0D14;
  border-left: 2px solid #296F44;
  padding: 10px;
  width: 500px;
  display: flex;
  align-items: center;
  margin-top: 20px;
}

.container form input {
  border: none;
  width: 100%;
  font-size: 16px;
  background-color: transparent;
}

.container form button {
  border: none;
  text-transform: uppercase;
  color: #359d5d;
  font-weight: bold;
  background-color: transparent;
  cursor: pointer;
}


.activies {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 10px;
  background-color: #BFC1CD;
  width: 500px;
  padding: 10px;

}

.activies p {
  background-color: transparent;
  color: #3f3f41;
  padding-left: 10px;
  font-weight: 500;
}

.activies .ajustar-imagem {
  display: flex;
  align-items: center;
  background-color: transparent;
  margin: 0;
}

.activies img {
  background-color: transparent;
  width: 15px;
  height: 12px;
  margin: 0;
  cursor: pointer;
}

.activies .delete {
  width: 13px;
  height: 15px;
  cursor: pointer;
}
</style>
