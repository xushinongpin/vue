### set 与 get

```
<!DOCTYPE html>
<html>
<head>
	<title>计算属性 setter 和 getter</title>
</head>
	<body>
		<div id="root">
			{{fullName}}
		</div>
	</body>
	<script src="./vue.js"></script>
	<script type="text/javascript">
		var vm = new Vue({
			el:"#root",
			data:{
				firstName: 'Dell',
				lastName: 'Lee'
			},
			computed: {
				fullName: {
					get: function() {
						return this.firstName + " " + this.lastName
					},
					set: function(value) {
						var arr = value.split(" ");
						this.firstName = arr[0]
						this.lastName = arr[1]
						console.log(value)
					}
				}
			}
		})
	</script>
</html>
```



