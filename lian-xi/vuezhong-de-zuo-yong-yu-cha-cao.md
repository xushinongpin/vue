# Vue中的作用域插槽

    <!DOCTYPE html>
    <html>
    	<head>
    		<meta charset="utf-8">
    		<title>Vue中的作用域插槽</title>
    	</head>
    	<body>
    		<div id="app">
    			<child>
    				<template slot-scope="props">
    					<li>{{props.item}}</li>
    				</template>
    			</child>
    		</div>
    	</body>
    	<script src="./vue.js"></script>
    	<script type="text/javascript">
    		Vue.component('child', {
    			data: function() {
    				return {
    					list: [1, 2, 3, 4]
    				}
    			},
    			template: `<div>
    						<ul>
    							<slot 
    								v-for="item of list"
    								:item=item
    							></slot>
    						</ul>
    					  </div>`
    		})
    		var vm = new Vue({
    			el: "#app",
    		})
    	</script>
    </html>



