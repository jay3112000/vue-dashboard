<template>
  <v-card class="w-0">
    <v-layout>
      <v-navigation-drawer
        
        class="bg-blue w-10"
        theme="dark"
        permanent
      >
        <v-list>
          <v-list-item
            prepend-avatar="https://avatars.githubusercontent.com/u/61292543?s=400&u=eb1102e5251ba0015f150168e30281cd9894b160&v=4"
            title="Jay Sharma"
            subtitle="jay@gmailcom"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-folder" title="My Portfolio" value="myfiles"></v-list-item>
          <v-list-item prepend-icon="mdi-account-multiple" title="Settings" value="shared"></v-list-item>
          <v-list-item prepend-icon="mdi-star" title="Profile" value="starred"></v-list-item>
        </v-list>
      </v-navigation-drawer>

      <v-main style="height: 30px"></v-main>
    </v-layout>
  </v-card>
</template>