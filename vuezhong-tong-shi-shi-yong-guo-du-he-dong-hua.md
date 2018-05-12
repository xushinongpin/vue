# Vue中同时使用过渡和动画

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Vue中同时使用过渡和动画</title>
		<link rel="stylesheet" type="text/css" href="./animate.css">
		<style type="text/css">
			.fade-enter,.fade-leave-to {
				opacity: 0;
			}
			.fade-enter-active,.fade-leave-active {
				transition: opacity 5s;
			}
		</style>
	</head>
	<body>
		<div id="app">
			<!-- <transition 
				type="transition"
				name="fade" 
				appear
				enter-active-class="animated shake fade-enter-active"
				leave-active-class="animated hinge fade-leave-active"
				appear-active-class="animated swing"
			>
				<div v-show="show">hello world</div>
			</transition> -->
			<transition 
				:duration="{enter: 10000 , leave: 5000}"
				name="fade" 
				appear
				enter-active-class="animated shake fade-enter-active"
				leave-active-class="animated hinge fade-leave-active"
				appear-active-class="animated swing"
			>
				<div v-show="show">hello world</div>
			</transition>
			<button @click="handdleClick">切换</button>
		</div>
	</body>
	<script src="./vue.js"></script>
	<script type="text/javascript">
		var vm = new Vue({
			el: "#app",
			data: {
				show: true
			},
			methods: {
				handdleClick: function() {
					this.show = !this.show
				}
			}
		})
	</script>
</html>
```



