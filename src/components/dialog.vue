<template>
    <div>
        <!-- <div class="dialog" v-show="show">
            <button @click="closeDialog">X</button>
        </div> -->
        <div class="dialog" v-show="show">
            <button @click="clickHandle">X</button>
        </div>
    </div>
</template>
<script>
export default {
    props:{
        show:{
            type: Boolean,
            default: false
        }
    },
    data(){
        return {
            // visiable: false
        }
    },
    methods: {
        // closeDialog(){
        //     this.$emit('update:show', false); //触发 input 事件，并传入新值
        // }
         clickHandle(){
            this.$emit('clickHandle'); //触发 input 事件，并传入新值
        }
    }
}
</script>
<style scoped>
.dialog {
    width: 100px;
    height: 100px;
    background-color: #000;
}

</style>