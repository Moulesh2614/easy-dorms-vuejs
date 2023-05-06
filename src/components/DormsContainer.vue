<template>
   
    {{doorms}}
    <div v-for="dorm of doorms.doorms" :key="dorm.id" >

     
       <DormsCard :dorm=dorm />

    </div>

</template>
<script>
import DormsCard from './DormsCard.vue'

export default {
    name: 'DormsContainer',
    props:{
        doorms: Array
    },
    components:{
        DormsCard
    }
    
}
</script>
<style >

</style>
