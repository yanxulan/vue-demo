<template>
    <div class="first-app">
        {{msg}}
        <confirm text="注册" @message="getMeaasge"></confirm>
        <p class="link">
            <router-link to="/second">去第二个页面</router-link>
        </p>
    </div>
</template>

<script>
import Confirm from "../sub/Confirm";
export default {
    name: "First",
    components: {
        Confirm
    },
    data() {
        return {
            msg: "Welcome to FirstApp"
        };
    },
    methods: {
        getMeaasge(val) {
            console.log(val);
        }
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less">
.first-app {
    font-size: 30px;
    .link {
        a {
            color: red;
        }
    }
}
</style>
