<script>
export default {
  data() {
    return {
      buttonText: 'Купити',
      type: 'normal',
      height: '32px',
      radius: '2px',
      paddingX: '8px',
      background: '#fff',
      borderColor: '#222',
      textColor: '#222',
      fontSize: '14px',
    }
  },
}
</script>

<template>
  <div class="wrapper">
    <div class="button-warapper">
      <button class="normal">{{buttonText}}</button>
    </div>
    <div class="option-item">
      <label>Текст кнопки</label><input type="text" v-model="buttonText" />
    </div>
    <div class="options">
      <!-- height -->

      <div class="option-item">
        <label for="height">Висота</label>
        <select name="height" id="height" v-model="height">
          <option value="24px">XS (24px)</option>
          <option value="32px">S (32px)</option>
          <option value="40px">M (40px)</option>
          <option value="48px">L (48px)</option>
        </select>
      </div>
      <!-- radius -->
      <div class="option-item">
        <label for="radius">Заокруглення</label>
        <select name="radius" id="radius" v-model="radius">
          <option value="0">None</option>
          <option value="2px">XS (2px)</option>
          <option value="4px">S (4px)</option>
          <option value="8px">M (8px)</option>
          <option value="12px">L (12px)</option>
          <option value="999px">Pill</option>
        </select>
      </div>
      <!-- padding -->
      <div class="option-item">
        <label for="paddingX">Відступи</label>
        <select name="paddingX" id="paddingX" v-model="paddingX">
          <option value="8px">S (8px)</option>
          <option value="12px">M (12px)</option>
          <option value="16px">L (16px)</option>
        </select>
      </div>

      <div class="option-item">
        <label>Розмір тексту</label><input type="text" v-model="fontSize" />
      </div>

      <div class="option-item">
        <label>Колір фону</label><input type="text" v-model="background" />
      </div>
      <div class="option-item">
        <label>Колір тексту</label><input type="text" v-model="textColor" />
      </div>
      <div class="option-item">
        <label>Колір бордеру</label><input type="text" v-model="borderColor" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  padding-top: 10rem;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.button-warapper {
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 128px;
  width: 320px;
  border-radius: 24px;
  margin-bottom: 24px;
}

.normal {
  outline: none;
  height: v-bind(height);
  padding: 0 v-bind(paddingX);
  font-size: v-bind(fontSize);
  background: v-bind(background);
  font-weight: 500;
  border-radius: v-bind(radius);
  border: 1px solid #222;
  border-color: v-bind(borderColor);
  color: v-bind(textColor);
}
.options {
  display: flex;
  flex-direction: column;
  gap: 8px;
  padding-top: 48px;
}

label {
  display: block;
  width: 128px;
}

.option-item {
  display: flex;
  align-items: center;
}

select,
input {
  outline: none;
  height: 32px;
  padding: 0 8px;
  margin-left: 10px;
  width: 128px;
  border: 1px solid #ccc;
  border-radius: 8px;
}
</style>
