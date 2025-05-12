<script>
export default {
  data() {
    return {
      type: 'normal',
      height: '32px',
      radius: '2px',
      paddingX: '8px',
      background: '#fff',
      borderColor: '#222',
      textColor: '#222',
    }
  },
}
</script>

<template>
  <div class="wrapper">
    <div class="button-warapper">
      <button class="normal">Купити</button>
    </div>

    <div class="options">
      <!-- height -->
      <div class="option-item">
        <label for="height">Висота</label>
        <select name="height" id="height" v-model="height">
          <option value="24px">XS</option>
          <option value="32px">S</option>
          <option value="40px">M</option>
          <option value="48px">L</option>
        </select>
      </div>
      <!-- radius -->
      <div class="option-item">
        <label for="radius">Заокруглення</label>
        <select name="radius" id="radius" v-model="radius">
          <option value="0">None</option>
          <option value="2px">S</option>
          <option value="4px">M</option>
          <option value="8px">L</option>
        </select>
      </div>
      <!-- padding -->
      <div class="option-item">
        <label for="paddingX">Відступи</label>
        <select name="paddingX" id="paddingX" v-model="paddingX">
          <option value="8px">S</option>
          <option value="12px">M</option>
          <option value="16px">L</option>
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
}

.normal {
  outline: none;
  height: v-bind(height);
  padding: 0 v-bind(paddingX);
  font-size: 1rem;
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

.radius-0 {
  border-radius: 0;
}

.radius-s {
  border-radius: 2px;
}

.radius-m {
  border-radius: 4px;
}

.radius-l {
  border-radius: 8px;
}

.height-xs {
  height: 24px;
}

.height-s {
  height: 32px;
}

.height-m {
  height: 40px;
}

.height-l {
  height: 48px;
}

.paddingX-s {
  padding: 0 8px;
}

.paddingX-m {
  padding: 0 12px;
}

.paddingX-l {
  padding: 0 16px;
}
</style>
