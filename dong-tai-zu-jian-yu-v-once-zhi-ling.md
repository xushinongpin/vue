# 动态组件与v-once指令

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>动态组件与v-once指令</title>
	</head>
	<body>
		<div id="app">
			<child-one v-if="type === 'child-one'"></child-one>
			<child-two v-if="type === 'child-two'"></child-two>
			<button @click="handleBtnClick">change</button>
			<component :is="type"></component>
		</div>
	</body>
	<script src="./vue.js"></script>
	<script type="text/javascript">
		Vue.component('child-one', {
			template: '<div v-once>child-one</div>'
		})
		Vue.component('child-two', {
			template: '<div v-once>child-two</div>'
		})
		var vm = new Vue({
			el: "#app",
			data: {
				type: 'child-one'
			},
			methods: {
				handleBtnClick: function() {
					this.type = (this.type === 'child-one' ? 'child-two' : 'child-one');
				}
			}
		})
	</script>
</html>
```



