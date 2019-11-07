<template>
  <view class="container">
    <AppLoading v-if="!loaded"/>
    <App v-else/>
  </view>
</template>

<script>
import Vue from "vue-native-core";
import { VueNativeBase } from "native-base";
import { AppLoading } from "expo";

import App from "../App.vue";

// registering all native-base components to the global scope of the Vue
Vue.use(VueNativeBase);

export default {
  components: { App, AppLoading },
  data() {
    return {
      loaded: false
    };
  },
  mounted () {
    setTimeout(() => {
      this.loaded = true
    }, 2000)
  }
};
</script>

<style>
.container {
  flex: 1;
}
</style>
