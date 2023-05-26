<template>
<div   class="cardBox" >
    <h1>
        Hi Jay , Welcome Back
    </h1>
  <v-card
    class="mx-auto"
    max-width="368"
  >
    <v-card-item title="Your Investment">
      
    </v-card-item>

    <v-card-text class="py-0">
      <v-row align="center" no-gutters>
        <v-col
          class="text-h3 text-red"
          cols="6"
        >
          12%
        </v-col>

        <v-col cols="6" class="text-right">
          <v-icon
            color="red"
            icon="mdi-menu-down"
            size="88"
          ></v-icon>
        </v-col>
      </v-row>
    </v-card-text>

    <div class="d-flex py-3 justify-space-between">
      <v-list-item
        density="compact"
      >
        <v-list-item-subtitle>Invested: 20k</v-list-item-subtitle>
      </v-list-item>

      <v-list-item
        density="compact"
      >
        <v-list-item-subtitle>Current: 15k</v-list-item-subtitle>
      </v-list-item>
    </div>

    <v-expand-transition>
      <div v-if="expand">
        <div class="py-2">
          <v-slider
            v-model="time"
            :max="6"
            :step="1"
            :ticks="labels"
            class="mx-4"
            color="primary"
            density="compact"
            hide-details
            show-ticks="always"
            thumb-size="10"
          ></v-slider>
        </div>

        <v-list class="bg-transparent">
          <v-list-item
            v-for="item in forecast"
            :key="item.day"
            :title="item.day"
            :append-icon="item.icon"
            :subtitle="item.temp"
          >
          </v-list-item>
        </v-list>
      </div>
    </v-expand-transition>

    <v-divider></v-divider>

    <v-card-actions>
      <v-btn @click="expand = !expand">
        {{ !expand ? 'Full Report' : 'Hide Report' }}
      </v-btn>
    </v-card-actions>
  </v-card>

  
</div>
</template>
<style lang="scss" scoped>
.cardBox{
    display: flex;
    flex-direction: column;
    width: fit-content;
    margin: auto;
    padding-left: 20%;
}
h1{
    margin-bottom: 40px;
    color: rgb(41, 177, 240);
    font-size: 30px;
}

</style>