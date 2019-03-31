<template>
    <div class="confirm">
        <button @click="getbuttonclick">{{text || '确认'}}</button>
    </div>
</template>
<script>
export default {
    name:'confirm',
    props:['text'],
    data(){
        return {
            msg:true
        }
    },
    methods:{
        getbuttonclick(){
            this.$emit("message",this.msg);
        }
    }
}
</script>
<style lang="less" scoped>
.confirm{
    font-size: 30px;
    .link{
        a{
            color: red;
        }
    }
}
</style>


