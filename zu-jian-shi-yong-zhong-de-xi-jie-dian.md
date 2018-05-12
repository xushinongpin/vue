# 组件使用中的细节点

```
<!DOCTYPE html>
<html>
	<head>
		<title>组件使用中的细节点</title>
	</head>
	<body>
		<div id="app">
			<table>
				<tbody>
					<tr is="row"></tr>
					<tr is="row"></tr>
					<tr is="row"></tr>
				</tbody>
			</table>
			<div 
				ref='hello'
				@click="handleClick"
			>
				hello world
			</div>
			<counter ref="one" @change="handleChange"></counter>
			<counter ref="two" @change="handleChange"></counter>
			<div>{{total}}</div>
		</div>
	</body>
	<script src="./vue.js"></script>
	<script type="text/javascript">
		Vue.component('row', {
			data: function() {
				return {
					content: "this is content"
				}
			},
			template: '<tr><td>{{content}}</td></tr>'
		})
		Vue.component('counter', {
			template: '<div @click="handleClickc">{{number}}</div>',
			data: function() {
				return {
					number: 0
				}
			},
			methods: {
				handleClickc: function() {
					this.number ++
					this.$emit('change')
				}
			}
		})
		var vm = new Vue({
			el: "#app",
			data: {
				total: 0
			},
			methods: {
				handleClick: function() {
					console.log(this.$refs.hello.innerHTML)
				},
				handleChange: function() {
					this.total = this.$refs.one.number + this.$refs.two.number
				}
			}
		})
	</script>
</html>
```



