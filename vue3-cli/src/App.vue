<template>
  <AppHeader :appTitle="message" v-on:change="changeMessage"></AppHeader>
  <div>
    {{ message }}
  </div>
  <button @click="showAlert">경고</button>
</template>

<script>
// import 컴포넌트이름 from '경로'
import AppHeader from './components/AppHeader.vue';

export default {
  components: {
    AppHeader,
  },
  data() {
    return {
      message: '앱 헤더 컴포넌트',
    };
  },
  methods: {
    showAlert() {
      alert('hi');
    },
    changeMessage() {
      this.message = '변경됨';
    },
  },
};
</script>

<style scoped></style>
