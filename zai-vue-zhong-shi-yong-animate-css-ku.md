# 在Vue中使用Animate.css库

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>在Vue中使用Animate.css库</title>
		<link rel="stylesheet" type="text/css" href="./animate.css">
		<!--官网提供的样式 可查找官网 bounce,flash,pulse,rubberBand,shake,swing,tada,wobble,jello,bounceIn,bounceInDown,bounceInLeft,bounceInRight,bounceInUp,bounceOut,bounceOutDown,bounceOutLeft,bounceOutRight,bounceOutUp,fadeIn,fadeInDown,fadeInDownBig,fadeInLeft,fadeInLeftBig,fadeInRight,fadeInRightBig,fadeInUp,fadeInUpBig,fadeOut,fadeOutDown,fadeOutDownBig,fadeOutLeft,fadeOutLeftBig,fadeOutRight,fadeOutRightBig,fadeOutUp,fadeOutUpBig,flip,flipInX,flipInY,flipOutX,flipOutY,lightSpeedIn,lightSpeedOut,rotateIn,rotateInDownLeft,rotateInDownRight,rotateInUpLeft,rotateInUpRight,rotateOut,rotateOutDownLeft,rotateOutDownRight,rotateOutUpLeft,rotateOutUpRight,slideInUp,slideInDown,slideInLeft,slideInRight,slideOutUp,slideOutDown,slideOutLeft,slideOutRight,zoomIn,zoomInDown,zoomInLeft,zoomInRight,zoomInUp,zoomOut,zoomOutDown,zoomOutLeft,zoomOutRight,zoomOutUp,hinge,jackInTheBox,rollIn,rollOut -->
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



