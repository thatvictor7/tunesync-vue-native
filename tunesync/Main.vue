<template>
  <view class="container">
    
    <text class="text-color-primary" :style="{color: 'rgb(66,133,244)', fontSize: 30}">TUNESYNC</text>
    <image
          :style="{width: 66, height: 58}"
          :source="{uri: 'https://i.pinimg.com/originals/bc/b9/7d/bcb97df2753cf719f37ca3687d0ff846.png'}"
        />
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
        color="#4285F4"
        accessibility-label="Learn more about this purple button"
    />
    </view>

</template>

<script>

console.log('aye')

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
      logo: './assets/tunesyncLogo.png'
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
  background-color: rgba(36, 36, 36, 0.973);
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: rgb(124, 124, 124);
}
.limit {
  background-color: rgb(29, 29, 29);
  color: rgb(255, 251, 251);
  width: 80%;
}
.login {
  margin-top: 5px;
  padding-top: 5px;
  background-color: aqua;
}
</style>