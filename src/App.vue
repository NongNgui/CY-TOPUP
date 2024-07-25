<template>
  <div>
    <h1>{{ title }}</h1>
    <h2>{{ count }}</h2>
    <button @click="checkCount">Click me Pls</button>
  </div>
</template>

<script>
export default {
  name: 'Main',
  data() {
    return {
      title: 'Click 100 ครั้งเพืื่อเป็นเกย์',
      count: 0
    }
  },
  methods: {
    checkCount() {
      this.count = this.count + 10
      if (this.count >= 100 && this.count < 10000) {
        this.title = 'เป็นเกย์แล้ว ลองกดอีก 10,000 ครั้งเพื่อกลับเป็นชาย'
      }
      else if (this.count >= 10000) {
        this.title = 'มึงนี้มันเกย์ตัวจริง'
      }
    }
  },
}
</script>

<style>

</style>