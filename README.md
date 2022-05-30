<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>综合示例演示注册</title>
	<script src="vue.js"></script>
</head>

<body>
	<div id="app" style="margin: 0 auto; width: 1200px;height: 700px;border: 1px solid #F8635C">
		<h2 style="text-align: center">填写个人信息</h2>
		<div style="width: 500px;float: left">
			<div style="margin-left: 30px">
				<form>
					姓名:<input type="text" name="user" v-model="user"><br><br>
					<fieldset style="margin-right: 30px">
						<legend>健康信息</legend>
						身高:<input type="text" v-model="height">体重:<input type="text" v-model="weight">
					</fieldset><br>
					性别:
					<input type="radio" value="男" v-model="sex">
					<label>男</label>
					<input type="radio" value="女" v-model="sex">
					<label>女</label><br><br>
					喜爱的运动:<br><br>
					<input type="checkbox" value="篮球" v-model="checkedNames">
					<label>篮球</label>
					<input type="checkbox" value="足球" v-model="checkedNames">
					<label>足球</label>
					<input type="checkbox" value="羽毛球" v-model="checkedNames">
					<label>羽毛球</label>
					<input type="checkbox" value="跑步" v-model="checkedNames">
					<label>跑步</label><br><br>
					<label>地址:</label>
					<select name="city" v-model="address">
						<option value="">请选择城市</option>
						<option value="北京">北京</option>
						<option value="上海">上海</option>
						<option value="广州">广州</option>
						<option value="深圳">深圳</option>
						<option value="杭州">杭州</option>
						<option value="四川">四川</option>
					</select>
					<br><br>
					个人简介:<br>
					<textarea v-model="profile" cols="50" rows="6">
						填写信息
					</textarea><br><br>
					<div style="text-align: center">
						<input type="submit" value="提交">
						<input type="reset" value="重置">
					</div>
				</form>
			</div>
		</div>
		<div style="width: 500px;float: right">
<!--
			<div style="margin-left: 30px">
				姓名:{{user}}<br><br><br>
				身高:{{height}}<br>
				体重:{{weight}}<br><br>
				性别:{{sex}}<br><br>
				喜爱的运动:{{checkedNames}}<br><br><br><br>
				地址:{{address}}<br><br>
				个人简介:{{profile}}
-->
			<img src="https://img.zcool.cn/community/01104658d0b1c4a801219c77c3253d.jpg@1280w_1l_2o_100sh.jpg" width="500" height="400" />
		    </div>
	  </div>
</div>
	<script src="vue.js"></script>
	<script type="text/javascript">
		var vm= new Vue({
			el:"#app",
			data: {
				user: '',
				height: '',
				weight: '',
				sex: '',
				checkedNames: [],
				address: '',
				profile: ''
			}
		})
	</script>
</body>
</html>
