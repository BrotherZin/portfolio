<template>
  <div id="lnb" class="header">
    <v-layout align-center>
      <div class="logo" justify-center align-center>
        An Hyeong Jin Portfolio
      </div>
      <v-spacer></v-spacer>
      <v-btn href="#profile" color="#eee" text>profile</v-btn>
      <v-btn href="#license" color="#eee" text>license</v-btn>
      <v-btn href="#career" color="#eee" text>Career</v-btn>
    </v-layout>
  </div>
</template>

<style scoped>
.header {
  position: fixed;
  top: 0px;
  width: 100%;
  z-index: 100;
  padding: 10px;
  color: #eee;
  background-color: black;
}
.header .logo {
  font-size: 20px;
  font-weight: bold;
  padding: 20px;
  color: #eee;
  background-color: black;
}
</style>