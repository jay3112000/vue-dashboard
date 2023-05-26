<template>
<fragment>
  <h1>Trending Players</h1>
  <v-sheet
    class="mx-auto"
    elevation="8"
    width="1000"
  >
    <v-slide-group
      v-model="model"
      class="pa-4"
      center-active
      show-arrows
    >
      <v-slide-group-item
        v-for="item in TrendingPlayers"
        :key="item.name"
        v-slot="{ isSelected, toggle }"
      >
        <v-card
          :color="isSelected ? 'primary' : 'grey-lighten-1'"
          class="ma-4"
          height="200"
          width="200"
          @click="toggle"
        >
        <div class="player">
          <div   class="player-icon">
            <v-icon
                size="98"
                icon="mdi-account"
              
              ></v-icon>
          </div>
          <h2>
            {{item.name}}
          </h2>
        </div>
        </v-card>
      </v-slide-group-item>
    </v-slide-group>
  </v-sheet>
  </fragment>
</template>

  
<script>
  export default {
    data () {
      return {
        TrendingPlayers: [
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
.player{
    display: flex;
    flex-direction: column;
    justify-items: center;
}
h1{
  font-size: 25px;
  margin-bottom: 20px;
}
.player-icon{
  width:50%;
  height: auto;
  margin: auto;

}
h2{
  font-size: 20px;
  text-align: center;
  margin: auto;
}
.select-buttons{
  display: flex;
  justify-content: space-evenly;
  width: 100%;
  margin-top: 20px;

}
.buy-btn{
  background-color: green;
  color: white;
  padding: 15px;
  border-radius: 10px;
  width: 50%;
  height: fit-content;
  margin: 1px;
}
.sell-btn{
  background-color: red;
  color: white;
  padding: 15px;
  border-radius: 10px;
  width: 50%;
  height: fit-content;
}

</style>