<template>
  <view class="page-container">
    <view class="login-box">
      <text class="title">{{ counter.count }}</text>
      <button type="primary" class="button" @click="onAdd">ADD</button>
      <!-- <nut-button type="primary" class="button" @click="onAdd">ADD</nut-button> -->

    </view>
  </view>
</template>

<script setup>
import { useCounterStore } from '../stores/counter'
import { Dongdong } from '@nutui/icons-vue-taro';
import { ref } from 'vue';


    const counter = useCounterStore()

    const onAdd = () => {
      counter.count++

      // with autocompletion ✨
      // counter.$patch({count: counter.count + 1})

      // or using an action instead
      // counter.increment()

}
</script>

<style>
.login-box {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  background-color: lightgray;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  padding: 20px;
}
.title {
  font-size: 32px;
}
.button {
  border: 1px solid lightgray;
  padding: 5px 10px;
  width: 100px;
  border: 1px solid blue;
}
</style>
