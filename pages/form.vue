<script setup lang="ts">
function send (event) {
  event.preventDefault(); // Предотвращаем стандартную отправку формы

  // Собираем данные формы
  const name = document.getElementById('name').value;
  const weight = document.getElementById('weight').value;
  const age = document.getElementById('age').value;
  const purpose = document.querySelector('input[name="purpose"]:checked').value;

  // Выводим собранные данные в консоль
  console.log('Имя:', name);
  console.log('Вес (кг):', weight);
  console.log('Возраст (лет):', age);
  console.log('Цель:', purpose);
};
</script>

<template>
<div class="container">
  <h1>Подбор программы</h1>
  <p>Заполните и мы подберем программу питания для вас и вашего кота</p>
  <form @submit.prevent="send">
    <div class="form-field">
      <label for="name">Имя:</label>
      <input type="text" id="name" name="name" required>
    </div>

    <div class="form-field">
      <label for="weight">Вес (кг):</label>
      <div><input type="text" id="weight" name="weight" required></div>
    </div>

    <div class="form-field">
      <label for="age">Возраст (лет):</label>
      <input type="text" id="age" name="age">
    </div>

    <div class="radio-section">
      <label>
        <input type="radio" name="purpose" value="loss" checked>
        Похудение
      </label>

      <label>
        <input type="radio" name="purpose" value="gain">
        Набор массы
      </label>

      <label>
        <input type="radio" name="purpose" value="advice">
        Не знаю (нужен ваш совет)
      </label>
    </div>

    <div class="form-field">
      <button type="submit">Отправить</button>
    </div>
  </form>
</div>
</template>

<style scoped>
.form-field {
  display: grid;
  grid-template-columns: minmax(40px, 100px) 1fr;
  margin-bottom: 15px;
  align-items: center;
  [type="text"] {
    border: 1px solid deepskyblue;
    box-sizing: border-box;
    padding: 10px;
    border-radius: 5px;
    margin-top: 5px;
    width: 100%;
  }
}
.form-field input[type=text] {

}
.form-field label {
  display: block;
}
.radio-section {
  margin: 20px 0;
  display: flex;
  flex-direction: column;
}
.radio-section label {
  margin-right: 10px;
}
</style>
