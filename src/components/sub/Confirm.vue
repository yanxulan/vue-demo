<template>
	<div class="confirm-button">
		<button @click="getButtonClick">{{text || '确认'}}</button>
	</div>
</template>

<script>
	export default {
        name: "confirm-button",
        props:["text"],
		data() {
			return {
                msg:true
            };
		},
		methods: {
			getButtonClick() {
				this.$emit("message", this.msg);   // 向父组件传递值
			}
		}
	};
</script>

<style>
	.confirm-button {
        margin-top: 100px;
	}
    .confirm-button button{
        width: 180px;
        height: 40px;
        font-size: 22px;
        background-color: aqua;
        outline: 0;
        border: 0;
        color: #fff;
        border-radius: 8px;
    }
</style>