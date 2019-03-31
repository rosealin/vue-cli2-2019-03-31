<template>
    <div class="first">
        {{msg}}
        <confirm text="注册" @message="getMessage"></confirm>
        <p><router-link to="/second">去第二个页面</router-link></p>
    </div>
</template>
<script>
import confirm from '../sub/confirm'
export default {
    name:'First',
    components:{
        confirm
    },
    data(){
        return{
            msg:'welcome to firstApp'
        }
    },
    methods:{
        getMessage(val){
            alert(val);
        }
    }
}
</script>
<style lang="less" scoped>
.first{
    font-size: 30px;
    a{
        color: red;
        text-decoration: none;
    }
}
</style>



