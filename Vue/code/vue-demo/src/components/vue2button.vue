<template>
    <div class="person">
        <h2>姓名：{{ name }}</h2>
        <h2>年龄：{{ age }}</h2>
        <h2></h2>
    </div>
</template>

<script>
    export default{
        data(){
            return{
                name:"Linus Andrew",
                age:24,
                tel:"16822658894"
            }
            
        }
    }
</script>