<script setup lang="ts">
import SideBar from './components/SideBar.vue'
import DashBoard from './components/DashBoard.vue'
import StatCards from './components/StatsCards.vue'
import DataTable from './components/DataTable.vue'
</script>

<template>
  <div>
    <SideBar/>
    <DashBoard/>
  </div>
  
</template>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #3f89d3;
  margin-top: 60px;
  width: 100%;

  background-color: white;
}
</style>
