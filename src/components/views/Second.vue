<template>
  <div class="second-app">
      {{msg}}
      <p><router-link to="/first">去第一个页面</router-link></p>
  </div>
</template>

<script>
import Confirm from '../sub/Confirm'
export default {
    name: "First",
    components: {
        Confirm
    },
    data() {
        return {
            msg: "Welcome to SecondApp"
        };
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
