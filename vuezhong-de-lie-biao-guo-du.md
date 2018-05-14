# Vue中的列表过渡

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Vue中的列表过渡</title>
		<style type="text/css">
			.v-enter,.v-leave-to {
				opacity: 0;
			}
			.v-enter-active,.v-leave-active {
				transition: opacity 1s;
			}
		</style>		
	</head>
	<body>
		<div id="app">
			<button @click="handleBtnClick">Add</button>
			<transition-group>
				<div v-for="item of list" :key="item.id">
					{{item.title}}
				</div>
			</transition-group>
		</div>
	</body>
	<script src="./vue.js"></script>
	<script type="text/javascript">
		var count = 0;
		var vm = new Vue({
			el: "#app",
			data: {
				list: []
			},
			methods: {
				handleBtnClick: function() {
					this.list.push({
						id: count++,
						title: 'hello world'
					})
				}
			}
		})
	</script>
</html>
```



