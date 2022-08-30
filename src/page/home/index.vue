<script setup lang="ts">
const state = reactive({
  height: 0,
})
onMounted(() => {
  // state.height = document.body.clientHeight
  state.height = document.querySelector('.fish-container')!.clientHeight
})
</script>

<template>
  <div class="fish-container">
    <iframe
      id="fishWin"
      src="https://wangrongding.github.io/jellyfish/"
      :height="state.height"
      frameborder="0"
      scrolling="no"
      sandbox="allow-same-origin allow-scripts allow-top-navigation allow-forms"
      width="100%"
    ></iframe>
    <div class="describe">
      <div class="content">
        <p>北故大学chsi项目</p>
        <p>
          原作者：https://github.com/wangrongding/frontend-park
        </p>
        <p>个人微信 →</p>
      </div>
      <img src="../../assets/qr.jpg" alt="" style="width: 200px" />
    </div>
  </div>
</template>

<style scoped lang="scss">
.fish-container {
  background-color: #91a8d0;
  height: 100%;
  position: relative;
  overflow: hidden;

  .describe {
    overflow: hidden;
    position: absolute;
    right: 50px;
    bottom: 50px;
    width: 600px;
    height: 200px;
    pointer-events: none;
    color: white;
    padding-left: 40px;
    box-sizing: border-box;
    border-radius: 40px;
    font-size: 14px;
    background: rgb(179 179 179 / 40%);
    display: flex;
    align-items: center;
    justify-content: space-around;
  }
}
</style>
