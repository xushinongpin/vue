# Vue中的Js动画与velocity.js

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Vue中的Js动画与velocity.js</title>
		<script type="text/javascript" src="./velocity.min.js"></script>
		<!-- 下载地址 http://velocityjs.org/ -->
	</head>
	<body>
		<div id="app">
			<transition 
				name="fade"
				@before-leave="handelBeforeEnter"
				@leave="handleEnter"
				@after-leave="handleAfterEnter"
			>
				<div v-show="show">hello world</div>
			</transition>
			<!-- <transition 
				name="fade"
				@before-enter="handelBeforeEnter"
				@enter="handleEnter"
				@after-enter="handleAfterEnter"
			>
				<div v-show="show">hello world</div>
			</transition> -->
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
				},
				/*handelBeforeEnter: function(el) {
					el.style.color = 'pink'
				},
				handleEnter: function(el, done) {
					setTimeout(() => {
						el.style.color = 'blue'
						done()
					}, 2000)
					setTimeout(() => {

					}, 4000)
				},
				handleAfterEnter: function(el) {
					el.style.color = 'green'
				}*/
				handelBeforeEnter: function(el) {
					el.style.opacity = 0;
				},
				handleEnter: function(el, done) {
					Velocity(el, {
						opacity:1
						}, {
							duration: 1000,
							complete: done
						}
					)
				},
				handleAfterEnter: function(el) {
					alert("动画结束")
				}
			}
		})
	</script>
</html>
```



