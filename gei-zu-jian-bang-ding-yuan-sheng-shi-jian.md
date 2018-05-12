# 给组件绑定原生事件

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>给组件绑定原生事件</title>
	</head>
	<body>
		<div id="app">
			<child @click="handleChick"></child>
			<child1 @click.native="handleChick"></child1>
		</div>
	</body>
	<script src="./vue.js"></script>
	<script type="text/javascript">
		Vue.component('child', {
			template: '<div @click="handleChildChick">Child</div>',
			methods: {
				handleChildChick: function() {
					this.$emit('click')
				}
			}
		})
		Vue.component('child1', {
			template: '<div>Child1</div>',
		})
		var vm = new Vue({
			el: "#app",
			methods: {
				handleChick: function() {
					alert('click')
				}
			}
		})
	</script>
</html>
```



