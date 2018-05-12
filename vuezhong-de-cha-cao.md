# Vue中的插槽（slot）

    <!DOCTYPE html>
    <html>
    	<head>
    		<meta charset="utf-8">
    		<title>Vue中的插槽（slot）</title>
    	</head>
    	<body>
    		<div id="app">
    			<child content='<p> world</p><p> dell</p>'></child>
    			<child1>
    				<!-- <h1>slotp</h1> -->
    			</child1>
    			<body-content>
    				<!-- <div class="header" slot="header">header</div> -->
    				<div class="footer" slot="footer">footer</div>
    			</body-content>
    		</div>
    	</body>
    	<script src="./vue.js"></script>
    	<script type="text/javascript">
    		Vue.component('child', {
    			props: ['content'],
    			template: '<div><p>hello</p><div v-html="this.content"></div></div>'
    		})
    		Vue.component('child1', {
    			template: '<div><p>slot </p><slot> 默认内容</slot></div>'
    		})
    		Vue.component('body-content', {
    			template: `<div>
    						<slot name="header"><h1>default header</h1></slot>
    						<div class="content">content</div>
    						<slot name="footer"></slot>
    					</div>`
    		})
    		var vm = new Vue({
    			el: "#app",
    		})
    	</script>
    </html>



