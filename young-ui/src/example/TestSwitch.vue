<template>
  <div>
    <y-switch v-model="active"></y-switch>
    <hr>
    <y-switch v-model="active" activeColor="red" inactiveColor="blue"></y-switch>

  </div>
</template>
<script>
import YSwitch from '@/components/switch/YSwitch'
export default {
  components:{
    YSwitch
  },
  data() {
    return {
      active:false
    }
  },

}
</script>