<template>
<div v-bind:class="msg" v-bind:id="msg2">测试</div>
<!-- 可以用:attr代替v-bind:attr来完成动态绑定 -->
<div :class="msg" :id="msg2">lk</div>
<!-- 当存在相同属性定义时，v-bind=""优先于其他属性绑定 -->
<!-- v-bind=""中已经生效的值无法再次绑定 -->
<button :disabled="isabled" v-bind="attrclass" >Click</button>
</template>

<script>

export default{
  data(){
    return{
      msg:"active",
      msg2:"ceshi",
      isabled:false,
      // 可以用数组来定义要绑定的属性
      // 需要注意的是数组的key值会直接反映为属性名称，
      // 如果这个属性名称在HTML语法中不存在，那么它将成为一个自定义的属性
      attrclass:{
        id:"attr",
        class:"appid",
        isabled:true,
        dynamicType:"UserDefined"
      }
    }
  }
}

</script>