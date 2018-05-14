# Vue中多个元素或组件的过渡

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Vue中多个元素或组件的过渡</title>
		<script type="text/javascript" src="./velocity.min.js"></script>
		<style type="text/css">
			.v-enter,v-leave-to{
				opacity: 0;
			}
			.v-enter-active,v-leave-active{
				transition: opacity 1s;
			}
		</style>
	</head>
	<body>
		<div id="app">
			<transition mode="in-out">
				<component :is="type"></component>
			</transition>
			<button @click="handdleClick">切换</button>
		</div>
	</body>
	<script src="./vue.js"></script>
	<script type="text/javascript">
		Vue.component('child',{
			template: '<div>child</div>'
		})
		Vue.component('child-one',{
			template: '<div>child-one</div>'
		})
		var vm = new Vue({
			el: "#app",
			data: {
				type: 'child'
			},
			methods: {
				handdleClick: function() {
					this.type = this.type === 'child' ? 'child-one' : 'child'
				},
			}
		})
	</script>
</html>
```



