# 组件参数校验与非props特性

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>组件参数校验与非props特性</title>
	</head>
	<body>
		<div id="app">
			<child content="hello world"></child>
		</div>
	</body>
	<script src="./vue.js"></script>
	<script type="text/javascript">
		Vue.component('child', {
			props: {
				content: {
					type: [ String , Number],
					required: false,
					default: 'default value',
					validator: function(value) {
						return (value.length > 5)
					}
				}
			},
			template: '<div>{{content}}</div>'
		})
		var vm = new Vue({
			el: "#app",
		})
	</script>
</html>
```



