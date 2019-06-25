<template>
  <div id="app">
    <div class="demo-image">
      <div class="block" v-for="fit in fits" :key="fit">
        <!--<span class="demonstration">{{ fit }}</span>-->
        <el-image
                style="width: 100px; height: 100px;float: left;"
                :src="url"
                :fit="fit"></el-image>
      </div>
    </div>
    <el-input v-model="input" placeholder="请输入内容"></el-input>
    <div>
      <el-button @click="startHacking">Start</el-button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    startHacking () {
      this.$notify({
        title: 'It works!',
        type: 'success',
        message: 'We\'ve laid the ground work for you. It\'s time for you to build something epic!',
        duration: 5000
      })
    },
    startHacking1 () {
      this.$notify({
        title: 'It!',
        type: 'success',
        message: 'We\'ve laid the ground work for you. It\'s time for you to build something epic!',
        duration: 5000
      })
    }


  },
  data() {
    return {
      input: '',
      fits: ['fill', 'contain', 'cover', 'none', 'scale-down'],
      url: 'https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg'
    }
  }

}
</script>


<style>
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
}
  #{
  
  }
</style>
