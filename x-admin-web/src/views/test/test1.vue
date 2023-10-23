<template>
  <div>
    <el-card id="file">
      <el-upload
        ref="upload-sql"
        action=''
        accept=".xlsx, .csv"
        :auto-upload="false"
        :on-change="changeFile"
        :http-request="uploadHandler">
        <el-button class="mr-2" plain slot="trigger" size="big">
          <i class="el-icon-upload mr-1 font-size-14"></i> 读取文件
        </el-button>支持 .xlsx 和 .csv表格文件上传
      </el-upload>

      <el-button @click="showImages" type="primary" icon="el-icon-s-opportunity" size = “big”>开始推荐</el-button>

    </el-card>
    <el-card id="img" style="height: 700px" class="app111">
      <img src="https://img1.imgtp.com/2023/09/22/xIZ7q6HG.jpg">
    </el-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showAllImages: false,
    }
  },
  components: {
    'el-image': 'https://element.eleme.cn/#/en-US/component/image'
  },
  methods: {
    showImages() {
      this.showAllImages = true;
    }
  }
};
</script>

<style scoped>

</style>
