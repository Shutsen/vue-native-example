<template>
  <view class="container">
    <button :title="message" :on-press="handleBtnPress"/>
  </view>
</template>

<script>
export default {
  data() {
    return {
      message: "Hello World!"
    }
  },
  methods: {
    handleBtnPress: function() {
      alert('Button pressed');
    }
  }
}
</script>

<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>
