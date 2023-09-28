<template>

<h3>模板语法</h3>
<p>{{ msg }}</p>
<!-- 计算 -->
<p>{{ number*5 }}</p>
<!-- 三目运算符结果返回 -->
<p>{{ ok?'Yes':'No' }}</p>
<!-- 字符串拆分、翻转、重新拼接 -->
<p>{{ message.split("").reverse().join("") }}</p>
<!-- 超链接的原始渲染、超链接渲染 -->
<p>{{ rawHtml }}</p>
<p v-html="rawHtml"></p>

</template>

<script>

export default{
  data(){
    return{
      msg:"magic",
      number:10,
      ok:true,
      message:'你好我好大家好',
      rawHtml:"<a href='https://www.baidu.com'>百度一下，你就知道</a>"
    }
  }
}

</script>