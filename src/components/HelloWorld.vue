<template>
  <div class="hello">
   <button @click="visiable=!visiable">按钮</button>
   <!-- <qdialog
   :show.sync='visiable' 
   ></qdialog> -->
   <qdialog
    :show='visiable'
    v-on:clickHandle="clickHandle"
   ></qdialog>
  </div>
</template>

<script>
import qdialog from '@/components/dialog.vue'
export default {
  name: 'HelloWorld',
  components: {
    qdialog
  },
  props: {
    msg: String
  },
  data(){
    return {
      visiable:false
    }
  },
  methods:{
    clickHandle(){
      console.log('777')
      this.visiable=false
    }
  }
}
</script>

<style scoped>
</style>
