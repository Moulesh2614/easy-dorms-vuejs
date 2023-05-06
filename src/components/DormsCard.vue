<template>
    
    <!-- {{dorm}} -->
<!-- {{ formattedDate }} -->
    <!-- <div  :class="dorm.lease_required ? 'green': 'red' "> -->
    <div class="card">

        <div>
            
            
            <h2><b>Area:</b> {{dorm.area}}</h2>
            <!-- <h4> {{dorm.rent_amount}}</h4> -->
            <h4>Rent Amount: {{ formattedRentAmount }}</h4>
            <h4>Deposit Amount: {{ formattedDepositAmount }}</h4>
            <h4>Available From: {{formattedDate}}</h4>
            
            <h4 v-if="dorm.lease_required == false" >Lease not required</h4>
            
            <h4 v-else>Lease Details: {{dorm.lease_details}}</h4>
            
        </div>
    </div>
</template>

<script>


export default{
    name: 'DormsCard',
    props:{
        dorm: Array,
        
    }
    
    , computed: {
        formattedDate() {
            
            const dateObj = new Date(this.dorm.available_from);
            
            const formattedDate = `${dateObj.getUTCMonth() + 1}-${dateObj.getUTCDate()}-${dateObj.getUTCFullYear()}`;
            return formattedDate;
            
    },
    formattedRentAmount(){
        const rentAmount =  this.dorm.rent_amount;
        const normalRentAmount = parseFloat(rentAmount["$numberDecimal"].toString());
        console.log(normalRentAmount); 
        return normalRentAmount;
    },
    formattedDepositAmount(){
        const depositAmount =  this.dorm.deposit_amount;
        const normaldepositAmount = parseFloat(depositAmount["$numberDecimal"].toString());
        console.log(normaldepositAmount); 
        return normaldepositAmount;
    }
}
    
}
</script>

<style scoped>

.green{
    background-color: green;
}

h4{
    margin: 2px;
}
.card{

}
div{
    background-color: white;
    color: black;
    padding: 1em;
    text-align: left;
    width: 50%;
    margin: auto;
    border-radius: 10px;

}

.red{
background-color: orangered !important;

}


</style>