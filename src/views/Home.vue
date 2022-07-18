<template>
  <div class="home">
    <wangButton>默认按钮</wangButton>
    <wangButton type="primary"  >成功按钮</wangButton>
    <wangButton type="danger" >危险按钮</wangButton>
    <wangButton type="warning" >警告按钮</wangButton>
  </div>
</template>

<script>

export default {
  name: 'Home',
  data () {
    return {
      flag: false
    }
  },
  components: {
    wangButton: () => import('../components/button/index.vue')
  },
  methods: {
    handleSubmit () {
      this.flag = true
      setTimeout(() => {
        console.log('666')
        this.flag = false
      }, 3000)
    }
  }
}
</script>
