<template>
  <!-- <app-navigation></app-navigation> -->
  <tab-nav></tab-nav>
</template>

<script>
// import { StackNavigator } from "vue-native-router";
import { TabNavigator,TabBarBottom } from "vue-native-router";
import MainScreen from './screens/Player'
import homeScreen from './screens/Search'
import PartyScreen from './screens/PartyScreen'
// const AppNavigation = StackNavigator(
//   {
//     Main: MainScreen,
//     homeScreen: homeScreen
//   },
//   {
//     initialRouteName: 'Main',
//   }
// );

const tabNav = TabNavigator(
  {
    'Your Music': MainScreen,
    Search: homeScreen,
    Party: PartyScreen
  },
  {
    tabBarPosition: "bottom",
    tabBarComponent: TabBarBottom
  }
);
export default {
    data(){
      return{
        user: [null,null]
      }
    },
    components: 
    // { AppNavigation }
    { tabNav }
}
</script>

