<script setup>
import { ref } from 'vue';
import ArcoVueIcon from '@arco-design/web-vue/es/icon';
import '@arco-design/web-vue/dist/arco.css';

defineProps({
  msg: String,
});

const count = ref(0);
let columns = ['City', 'IP'];
let vps_status = [
  { ip: 'xxx', city: 'cccc' },
  { ip: '1.2023yy', city: 'cccc' },
];
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>
  <ul v-for="info in vps_status">
    <span> {{ info.ip }} </span>
    <span> {{ info.city }} </span>
  </ul>
  <list v-for="info in vps_status" :data="info.city" />
  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Install
    <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>
    in your IDE for a better DX
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
