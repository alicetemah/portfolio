<template>
  <div>
    <Portfolio/>
  </div>      
</template>

<script lang="ts" setup>
import {defineComponent} from 'vue';
import Portfolio from './views/portfolio.vue';


const component =defineComponent({
  components:{
    Portfolio

  }

})

</script>
