<template>
  <view class="center">
    <text-input
        :style="{height: 40, borderColor: 'gray', borderWidth: 1, width: '95%'}"
        v-model="text"
      />
  </view>
</template>

<script>
export default {
  props: {
    navigation: {
      type: Object
    }
  },
  data: function() {
            return {
                text: ''
            };
  }
}
</script>

<style>
.center {
  background-color: rgba(255, 255, 255, 0.973);
  align-items: center;
  /* justify-content: center; */
  flex: 1;
  padding-top: 10%;
}
</style>


