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

      <el-button @click="showImages" type="primary" icon="el-icon-s-opportunity" size = “big”>统计显示</el-button>

    </el-card>
    <el-card id="img" style="height: 700px" class="app111">
      <!--      <el-image style="width: 160px; height: 100px" :src="require('~@/../src/assets/仓库1.jpg')"></el-image>-->
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
