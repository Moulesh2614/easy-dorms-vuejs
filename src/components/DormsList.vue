<template>
    <!-- {{doorms}} -->
    <div v-for="dorm of doorms" :key="dorm._id" >

        <!-- <h1>{{dorm.area}}</h1> -->
        <DormsCard :dorm=dorm />

    </div>
</template>
<script>
import DormsCard from './DormsCard.vue'

export default {
    name: 'DormsList',
    props:{
        doorms: Array
    }
    ,
    components:{
        DormsCard
    }
    
}
</script>
<style >
/* div{
    background-color: brown;
    
} */
</style>