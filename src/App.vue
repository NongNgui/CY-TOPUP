<template>
  <Header></Header>
  <div>
    <h1>{{ title }}</h1>
    <h2>{{ count }}</h2>
    <button @click="checkCount">Click me Pls</button>
  </div>
</template>

<script>
import Header from './components/Header.vue';
export default {
  name: 'Main',
  components: {
    Header
  },
  data() {
    return {
      title: 'ตอนนี้มึงเป็นเกย์ Click 100 ครั้งเพื่อกลับเป็นชายแท้',
      count: 0
    }
  },
  methods: {
    checkCount() {
      this.count = this.count + 100
      if (this.count >= 100 && this.count < 10000) {
        this.title = 'เป็นเกย์แล้ว ลองกดอีก 10,000 ครั้งเพื่อกลับเป็นชาย'
      }
      else if (this.count >= 10000 && this.count < 5000000) {
        this.title = 'มึงนี้มันเกย์ตัวจริง ลองกดอีก 5,000,000'
      }
      else if (this.count >= 5000000) {
        this.title = 'มึงนี้มันเกย์ตัวจริง ลองกดอีก 5,000,000'
      }
    }
  },
}
</script>

<style>

</style>