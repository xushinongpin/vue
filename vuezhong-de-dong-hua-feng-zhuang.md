# Vue中的动画封装

    <!DOCTYPE html>
    <html>
    	<head>
    		<meta charset="utf-8">
    		<title>Vue中的动画封装</title>	
    	</head>
    	<body>
    		<div id="app">
    			<button @click="handleBtnClick">change</button>
    			<fade :show="show">
    				<div>hello world</div>
    			</fade>
    			<fade :show="show">
    				<h1>hello world</h1>
    			</fade>
    		</div>
    	</body>
    	<script src="./vue.js"></script>
    	<script type="text/javascript">
    		Vue.component('fade', {
    			props: ['show'],
    			template: `
    				<transition @before-enter="handleBeforeEnter"  
    					@enter="handleEnter">
    					<slot v-if="show"></slot>
    				</transition>
    			`,
    			methods: {
    				handleBeforeEnter: function(el) {
    					el.style.color = 'red'
    				},
    				handleEnter: function(el, done) {
    					setTimeout(() => {
    						el.style.color = 'green'
    						done()
    					}, 2000)
    				}
    			}
    		})
    		var vm = new Vue({
    			el: "#app",
    			data: {
    				show: false
    			},
    			methods: {
    				handleBtnClick: function() {
    					this.show = !this.show
    				},
    			}
    		})
    	</script>
    </html>



