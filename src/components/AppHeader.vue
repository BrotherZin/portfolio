<template>
  <div class="header">
    <v-layout align-center>
      <div class="logo" justify-center align-center>
        An Hyeong Jin Portfolio
      </div>
      <v-spacer></v-spacer>
      <v-btn window.location.href="profile" color="#eee" text>profile</v-btn>
      <v-btn id="2" color="#eee" text>license</v-btn>
      <v-btn id="3" color="#eee" text>project 3</v-btn>
    </v-layout>
  </div>
</template>

<style scoped>
.header {
  padding: 20px;
  box-shadow: 0 6px 6px #eee;
  background-color: black;
}
.header .logo {
  font-size: 20pxl;
  font-weight: bold;
  color: #eee;
}
</style>