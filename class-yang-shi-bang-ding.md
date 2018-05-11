样式绑定

```
<!DOCTYPE html>
<html>
	<head>
		<title>vue中的样式绑定</title>
		<style type="text/css">
			.activated{color: red;font-size: 24px}
			.activate{color: pink;font-size: 24px}
		</style>
	</head>
	<body>
		<div id="app">
			<div @click="handleDivClick" :class="{activated: isActivated}">hello word</div>
			<div @click="handleDivClickd" :class="[activate]">hello word</div>
		</div>
	</body>
	<script src="./vue.js"></script>
	<script type="text/javascript">
		var vm = new Vue({
			el: "#app",
			data: {
				isActivated: false,
				activate: false,
			},
			methods: {
				handleDivClick: function() {
					this.isActivated = !this.isActivated;
					
				},
				handleDivClickd: function() {
					this.activate = this.activate === "activate" ? "" : "activate";
					
				},
			}
		})
	</script>
</html>
```



