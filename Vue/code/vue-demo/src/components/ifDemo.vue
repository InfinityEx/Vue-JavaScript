<template>
    <h3>Can you see me?</h3>
    <!-- v-if与v-show的区别 -->
    <!-- v-if在表达式不成立时，可以输出v-else的元素 -->
    <!-- 但v-show的表达式只能控制自己 -->
    <!-- 同时v-if是'真实的'按照条件渲染的，条件区块内的事件监听器和子组件都会被销毁与重建 -->
    <!-- 也就意味着如果条件不成立，v-if甚至不会被渲染，直到条件为真 -->
    <!-- 而v-show则不同，无论条件是否成立，在页面加载时v-show就会被渲染-->
    <!-- 和v-if不同，v-show的显示与否取决于CSS的display值 -->
    <div v-if="flag">show me your Kungfu</div>
    <div v-else>Sandburn!</div>
    <h3>It's time for Rock</h3>
    <div v-if="type==='A'">HeiHeiHei!</div>
    <div v-else-if="type==='B'">ikuzei!</div>
    <div v-else-if="type==='C'">hahahahaha</div>
    <div v-show="flag">Hadouken!</div>
</template>

<script>
export default{
    data(){
        return{
            flag:false,
            type:"B"
        }
    }
}
</script>