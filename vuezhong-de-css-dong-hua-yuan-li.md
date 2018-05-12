# Vue中的CSS动画原理

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Vue中的CSS动画原理</title>
		<style type="text/css">
			.fade-enter,.fade-leave-to,.v-leave-to,.v-enter{
				opacity: 0;
			}
			.fade-enter-active,.fade-leave-active,.v-leave-active,.v-enter-active{
				transition: opacity 1s
			}
		</style>
	</head>
	<body>
		<div id="app">
			<transition name="fade">
				<div v-if="show">hello world</div>
			</transition>
			<transition>
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



