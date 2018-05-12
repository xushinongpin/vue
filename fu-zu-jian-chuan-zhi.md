# 父组件传值

```
<!DOCTYPE html>
<html>
	<head>
		<title>父组件传值</title>
	</head>
	<body>
		<div id="app">
			<counter :count="0" @inc="handleIncrease"></counter>
			<counter :count="0" @inc="handleIncrease"></counter>
			<div>{{total}}</div>
		</div>
	</body>
	<script src="./vue.js"></script>
	<script type="text/javascript">
		//父可以改子，子不可以改父
		var counter = {
			props: ['count'],
			data: function() {
				return {
					number: this.count
				}
			},
			template: '<div @click="handleClick">{{number}}</div>',
			methods: {
				handleClick: function() {
					this.number ++;
					this.$emit('inc',1);
				}
			}
		}
		var vm = new Vue({
			el: "#app",
			data: {
				total: 0
			},
			components: {
				counter: counter
			},
			methods: {
				handleIncrease: function(step) {
					this.total += step;
				}
			}
		})
	</script>
</html>
```



