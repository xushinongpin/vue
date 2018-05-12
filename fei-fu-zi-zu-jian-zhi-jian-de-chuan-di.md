# 非父子组件之间的传递\(Bus/总线/发布订阅模式/观察者模式\)

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>非父子组件之间的传递(Bus/总线/发布订阅模式/观察者模式)</title>
	</head>
	<body>
		<div id="app">
			<child content="Dell"></child>
			<child content="Lee"></child>
		</div>
	</body>
	<script src="./vue.js"></script>
	<script type="text/javascript">
		Vue.prototype.bus = new Vue()
		Vue.component('child', {
			data: function() {
				return {
					selfContent: this.content
				}
			},
			props: {
				content: String
			},
			template: '<div @click="handleClick">{{selfContent}}</div>',
			methods: {
				handleClick: function() {
					this.bus.$emit('change', this.selfContent)
				}
			},
			mounted: function() {
				var this_ = this
				this.bus.$on('change', function(msg) {
					this_.selfContent = msg
				})
			}
		})
		var vm = new Vue({
			el: "#app",
		})
	</script>
</html>
```



