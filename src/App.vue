
<template>
  <div class="counter-container">
    <div class="counter-card">
      <h1>شمارنده من</h1>

      <div class="counter-number">
        {{ count }}
      </div>

      <div class="buttons">
        <button class="btn increase" @click="count++">
          +
        </button>

        <button class="btn decrease" @click="count--">
          −
        </button>

        <button class="btn reset" @click="count = 0">
          صفر کردن
        </button>
      </div>

      <p class="message">
        مقدار شمارنده: {{ count }}
      </p>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)
</script>

<style>
* {
  box-sizing: border-box;
}

.counter-container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #f1f5f9;
  font-family: Tahoma, Arial, sans-serif;
  direction: rtl;
}

.counter-card {
  background: white;
  padding: 35px;
  border-radius: 20px;
  text-align: center;
  width: 320px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.counter-card h1 {
  color: #334155;
  font-size: 24px;
  margin-bottom: 20px;
}

.counter-number {
  font-size: 70px;
  font-weight: bold;
  color: #2563eb;
  margin: 20px 0;
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 10px;
  flex-wrap: wrap;
}

.btn {
  border: none;
  border-radius: 10px;
  padding: 12px 20px;
  font-size: 22px;
  cursor: pointer;
  color: white;
  transition: 0.2s;
}

.btn:hover {
  transform: scale(1.05);
}

.increase {
  background: #22c55e;
}

.decrease {
  background: #ef4444;
}

.reset {
  background: #64748b;
  font-size: 16px;
}

.message {
  margin-top: 25px;
  color: #64748b;
  font-size: 15px;
}
</style>
