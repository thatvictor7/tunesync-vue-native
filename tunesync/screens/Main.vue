<template>
  <view class="container">
    
    <!-- <text class="text-color-primary" :style="{color: 'rgb(66,133,244)', fontSize: 30}">TUNESYNC</text> -->
    <!-- <view class="soft"> -->
    <image
          :style="{width: 400, height: 75}"
          :source="logo"
        />
    <!-- </view> -->
    <text class="text-color-primary">Username:</text>
    <text-input
        :style="{height: 40, borderColor: 'gray', width: '70%',marginTop: 8, marginBottom: 8}"
        class="limit"
        v-model="username"
      />
      <text class="text-color-primary">Password:</text>
      <text-input
        :style="{height: 40, borderColor: 'gray', width: '70%',marginTop: 8, marginBottom: 12}"
        class="limit"
        v-model="myInput"
      />
      <button
        :style="{marginTop: 24}"
        :on-press="handleButton"
        title="Login"
        color="#0B85E3"
        accessibility-label="Learn more about this purple button"
    />
    </view>

</template>

<script>
import logo from '../assets/tunesyncLogo.png'

export default {
props: {
    navigation: {
    type: Object
    }
  },
  data() {
    return{
      username: "",
      message: "whatttt",
      myInput: '',
      logo
    }
  },
  methods: {
    handleButton() {
      this.myInput = "Button clicked"
      this.navigation.navigate("homeScreen");
    }
  }
  
}


</script>
 
<style>
.container {
  background-color: rgba(255, 255, 255, 0.959);
  align-items: center;
  justify-content: center;
  flex: 1;
  width: 100%;
  height: 100%;
}
.text-color-primary {
  color: rgb(124, 124, 124);
}
.limit {
  background-color: rgba(172, 172, 172, 0.219);
  color: rgb(255, 251, 251);
  width: 80%;
  border-radius: 3;
  text-decoration-line: none;
}
.login {
  margin-top: 5px;
  padding-top: 5px;
  background-color: aqua;
}
</style>