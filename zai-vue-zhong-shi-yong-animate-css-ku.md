# 在Vue中使用Animate.css库

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>在Vue中使用Animate.css库</title>
		<link rel="stylesheet" type="text/css" href="./animate.css">
		<style type="text/css">
			/*官方网址 https://daneden.github.io/animate.css/*/
			/*@keyframes bounce-in {
				0% {
					transform: scale(0);
				}
				50% {
					transform: scale(1.5);
				}
				100% {
					transform: scale(1);
				}
			}*/
			/*.active {
				transform-origin: left center;
				animation: bounce-in 1s;
			}
			.leave {
				transform-origin: right center;
				animation: bounce-in 1s reverse;
			}*/
			/*.fade-enter,.fade-leave-to,.v-leave-to,.v-enter{
				opacity: 0;
			}
			.fade-enter-active,.fade-leave-active,.v-leave-active,.v-enter-active{
				transition: opacity 1s
			}*/
		</style>
	</head>
	<body>
		<div id="app">
			<!-- <transition name="fade" 
				enter-active-class="active"
				leave-active-class="leave"
			>
				<div v-show="show">hello world</div>
			</transition> -->
			<transition name="fade" 
				enter-active-class="animated shake"
				leave-active-class="animated hinge"
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



