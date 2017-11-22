<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<div id="app"></div>
		<div id="app2"></div>
	</body>
	<script type="text/javascript" src="react.min.js"></script>
	<script type="text/javascript" src="react-dom.js"></script>
	<script type="text/javascript">
		//创建ul虚拟dom
//		var ul = React.createElement(
//			'ul',
//			null,
//			//创建第一个li
//			React.createElement(
//				'li',
//				null,
//				'女装/男装/内衣'
//			),
//			//创建第二个li
//			React.createElement(
//				'li',
//				null,
//				'鞋靴/箱包/配件'
//			),
//			//创建第三个li
//			React.createElement(
//				'li',
//				null,
//				'童装玩具/孕产/用品'
//			)
//		);
		//创建组件
		var uls = React.createClass({
			render: function () {
				//通过return返回一个组虚拟dom树
				return React.createElement(
					'ul',
					null,
					//创建第一个li
					React.createElement(
						'li',
						null,
						'女装/男装/内衣'
					),
					//创建第二个li
					React.createElement(
						'li',
						null,
						'鞋靴/箱包/配件'
					),
					//创建第三个li
					React.createElement(
						'li',
						null,
						'童装玩具/孕产/用品'
					)
				)
			}
		})
		console.log(uls);
		//将组件转化成虚拟dom
		var ul = React.createElement(uls);
		//将虚拟dom渲染到页面中
		ReactDOM.render(ul,document.getElementById('app'));
		//通过组件创建一个新的虚拟dom
		var ul2 = React.createElement(uls);
		ReactDOM.render(ul, document.getElementById('app2'));
	</script>
</html>
