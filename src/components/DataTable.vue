<template>
<div class="w-50 ml-auto d-flex flex-column ">
  <v-table >
     
    <thead>
      <tr>
        <th class="text-left">
          Player Name
        </th>
        <th class="text-left">
          Buy Price
        </th>
         <th class="text-left">
          Current Price
        </th>
        <th class="text-left">
          P/L
        </th>
      </tr>
    </thead>
    <tbody>
      <tr
        v-for="item in players"
        :key="item.name"
      >
        <td>{{ item.name }}</td>
        <td>{{ item.buy }}</td>
        <td>{{ item.current }}</td>
        <td :class="[item.buy>item.current?'loss':'profit']">{{ calculatePL(item.buy,item.current) }}%</td>
      </tr>
    </tbody>
  </v-table>
</div>
</template>
<script>
  export default {
    data () {
      return {
        players: [
          {
            name: 'Rohit Sharma',
            buy: 159,
            current:160,
          },
          {
            name: 'Virat Kohli',
            buy: 237,
            current:160,
          },
          {
            name: 'KL rahul',
            buy: 262,
            current:160,
          },
          {
            name: 'Hardik Pandya',
            buy: 305,
            current:160,
          },
          {
            name: 'Ben Stokes',
            buy: 356,
            current:160,
          },
          {
            name: 'Chris Gayle',
            buy: 375,
            current:160,
          },
          
        ],
      }
    },
    methods:{
        calculatePL(buyPrice,currentPrice){
            return Math.floor((currentPrice-buyPrice)/buyPrice *100)
        }
    }
  }

</script>
<style scoped>
.profit{
    color: green;
}
.loss{
    color: red;
}
.primaryText{
    color:blue
}

</style>