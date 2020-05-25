<template>
	<div id="app">
		<Header></Header>
		<div class="theme">
			<Button @click="myFn('theme')"></Button>
			<Button @click="myFn('theme1')"></Button>
			<Button @click="myFn('theme2')"></Button>
		</div>
	</div>
</template>
<script>
import Header from "./components/Header";
export default {
	name: "App",
	components: {
		Header
	},
	methods: {
		myFn(data) {
			// console.log(data);
			document.documentElement.setAttribute("data-theme", data);
		}
	}
};
</script>
<style scoped lang="scss">
@import "assets/css/variable";

.theme {
	position: fixed;
	left: 0;
	bottom: 0;
	button {
		width: 100px;
		height: 100px;
		// background: #000;
		&:nth-of-type(1) {
			background: $background-color-theme;
		}
		&:nth-of-type(2) {
			background: $background-color-theme1;
		}
		&:nth-of-type(3) {
			background: $background-color-theme2;
		}
		background: #000;
	}
}
</style>
