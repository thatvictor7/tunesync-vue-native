<template>
  <app-navigation></app-navigation>
</template>

<script>
import { StackNavigator } from "vue-native-router";
import MainScreen from './Main'
import homeScreen from './homeScreen'
const AppNavigation = StackNavigator(
  {
    Main: MainScreen,
    homeScreen: homeScreen
  },
  {
    initialRouteName: 'Main',
  }
);
export default {
    components: { AppNavigation }
}
</script>