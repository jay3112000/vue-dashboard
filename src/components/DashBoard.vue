<template>
    <div id="dashboard">
        <div class="dashboard-upper"> 
            <StatCards/>
            <DataTable/>
        </div>
        <div class="dashboard-lower"> 
            <TrendingCards/>
        </div>
        
    </div>
</template>

<script>
import DataTable from './DataTable.vue'
import StatCards from './StatsCards.vue'
import TrendingCards from './TrendingCards.vue'
    export default {
        components:{
            DataTable,StatCards,TrendingCards
        }
    }
</script>

<style lang="scss" scoped>
#dashboard{
 display: flex;
 flex-direction: column;
}
.dashboard-upper{
    background-color: white;
    width: 100;
    display: flex;
    justify-content: space-evenly;
}
.dashboard-lower{
    margin: 30px 190px;
    padding-left: 20%;
    display: flex;
    justify-content: center;
}
h1{
    color: black;
}
</style>