<template>
    <view class="center">
        <text class="button1"
              :on-press="onPressLearnMore">
            Create Party
        </text>
        <text class="button1"
              :on-press="onPressLearnMore">
            Join Party
        </text>
        <text class="bottom">no
        </text>
    </view>
</template>

<script>
export default {
    methods: {
        onPressLearnMore: function() {
            alert('Hello')
        }
    }
}
</script>

<style>
.center {
  align-items: center;
  /* justify-content: center; */
  flex: 1;
  background-color: rgb(255, 255, 255);
  margin-top: 10%;
}
.button1 {
    color: white;
    font-size: 20;
    background-color: #0B85E3;
    padding: 10;
    margin: 6;
    border-radius: 2;
    align-items: center;
    justify-content: center;
}
.bottom {
    border-bottom-color: black;
    background-color: rgb(0, 188, 204);
    width: 100%;
    height: 2;
}
</style>