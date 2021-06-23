<template>
  <div class="home">
    <div style="display: flex;padding: 10px;background: white;position: fixed;width: 100%;top:0">
      <div style="padding-right: 10px;">
        <img src="../img/heart.png">
      </div>
      <div>
        <div style="font-size: 18px;">更多优质单身男女</div>
        <div style="font-size: 12px;color: #919090">看这里</div>
      </div>
    </div>
    <div style="margin-top:70px;"></div>
    <div style="background: white;border-radius: 10px;margin: 8px;" v-for="(item, key) in userInfoList" :key="key">
      <div><img style="width: 100%" src="../img/photo.png"></div>
      <div style="padding: 10px 6px;">
        <div>爱好：足球、足球、足球</div>
        <div>关于我：期望期望期望期望期望期望期望期望期望期望期望</div>
        <div>期望你：期望期望期望期望期望期望期望期望期望期望期望期望期望</div>
      </div>
    </div>
    <div style="display: flex;justify-content: center;margin: 30px;">
      <el-button style="width: 200px;" type="primary">更多单身男女....</el-button>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    // HelloWorld
  },
  data(){
    return {
      userInfoList: [1,2,3]
    }
  }
}
</script>
<style scoped>

</style>
