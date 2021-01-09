<template>
  <div class="hello">
    <div class="block">

  <!-- <span class="demonstration">默认 click 触发子菜单12</span> -->
  <!-- <el-cascader
    v-model="value"
    :options="options"
    @change="handleChange"></el-cascader> -->
    

    <!-- <div class="imageFrame">
    <input name="upimage" id="upimage" type="file">
    <input type="button" id="upimageButton" onclick="upimage.click()">
    <img id="showimage" src="" alt="">
    </div> -->

</div>
  </div>
</template>

<script>
import '../../public/exif.min';
import compressImg from '../../public/processImg'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
   mounted () {
      compressImg('upimage','showimage',480,function(src){
        //此处为回调函数，当图片压缩完成并成功显示后执行
        //可得到图片数据值src
        console.log(src);
  });
   },
  created () {
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
