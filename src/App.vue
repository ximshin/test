<script>
export default {
  data() {
    return {
      buttonText: 'Купити',
      type: 'normal',
      heightValue: '40px',
      fontWeight: '500',
      height: [
        '24px',
        '28px',
        '32px',
        '36px',
        '40px',
        '44px',
        '48px',
        '52px',
        '56px',
        '60px',
        '64px',
      ],
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
      <button class="normal">{{ buttonText }}</button>
    </div>
    <div class="option-item">
      <label>Текст кнопки</label><input type="text" v-model="buttonText" />
    </div>
    <div class="options">
      <!-- height -->

      <div class="option-item">
        <label for="height">Висота</label>
        <select name="height" id="height" v-model="heightValue">
          <option v-for="(value, idx) in height" :key="idx" :value="value">{{ value }}</option>
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
        <label for="fontWeight">Жирність</label>
        <select name="fontWeight" id="fontWeight" v-model="fontWeight">
          <option value="500">Нормальний</option>
          <option value="600">Жирний</option>
        </select>
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
  padding: 24px;
  box-sizing: border-box;
}

.normal {
  outline: none;
  height: v-bind(heightValue);
  font-size: v-bind(fontSize);
  background: v-bind(background);
  font-weight: v-bind(fontWeight);
  border-radius: v-bind(radius);
  border: 1px solid #222;
  border-color: v-bind(borderColor);
  color: v-bind(textColor);
  box-sizing: border-box;
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
