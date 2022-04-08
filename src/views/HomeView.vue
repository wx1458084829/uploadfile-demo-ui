<template>
  <div class="home">
<el-upload
    list-type="picture-card"
    action="http://127.0.0.1:3000/up-file/"
    multiple
    :limit="3"
    name = "file-name"
    :on-success="handleSucess"
  >
    <el-button type="primary">Click to upload</el-button>
    <template #tip>
      <div class="el-upload__tip">
        jpg/png files with a size less than 500KB.
      </div>
    </template>
  </el-upload>

  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'HomeView',
  components: {
  },data() {
    return {
      
    }
  },methods:{
handleSucess(response,uploadFile,uploadFiles){
  console.log(response);
}
  }
}
</script>
