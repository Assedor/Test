<!DOCTYPE html>
<html>
<head>
	<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
	<meta name="viewport" content="initial-scale=1.0, user-scalable=no" />
	<style type="text/css">
		body, html{width: 100%;height: 100%;margin:0;font-family:"微软雅黑";font-size:25px;}
		#l-map{height:700px;width:100%;}
		#r-result{width:100%;}
	</style>
	<script type="text/javascript" src="http://api.map.baidu.com/api?v=2.0&ak=GvSKKGSozB4c63CykzvGUjOBhfSsFuuS"></script>
	<title>关键字输入提示词条</title>
</head>
<body>
	<div id="l-map"></div>
	<div id="rr"></div>
	<div id="r-result" align=center>查询地点请输入:<input type="text" id="suggestId" size="20" value="" style="width:150px;" /></div>
	<div id="searchResultPanel" style="border:1px solid #C0C0C0;width:150px;height:auto; display:none;"></div>
	
	<div id="get1" align=center>
	步行路线规划：起点<input type="text" id="start" size="20">
	终点<input type="text" id="destiny" size="20">
	<input type="button" id="result" value="查询" onclick="searchwalkRoute(this)">
	</div>
	
	<div id="get3" align=center>
	私家车路线规划：起点<input type="text" id="start2" size="20">
	终点<input type="text" id="destiny2" size="20">
		<select id="driving_way">
			<option value="0">最少时间</option>
			<option value="1">最短距离</option>
			<option value="2">避开高速</option>
		</select>
	<input type="button" id="result2" value="查询" onclick="searchcarRoute(this)">
	</div>
</body>
</html>
<script type="text/javascript">

	function G(id) {
		return document.getElementById(id);
	}

	var map = new BMap.Map("l-map");
	map.centerAndZoom("杭州",12);                   

	var ac = new BMap.Autocomplete(    
		{"input" : "suggestId"
		,"location" : map
	});

	ac.addEventListener("onhighlight", function(e) { 
	var str = "";
		var _value = e.fromitem.value;
		var value = "";
		if (e.fromitem.index > -1) {
			value = _value.province +  _value.city +  _value.district +  _value.street +  _value.business;
		}    
		str = "FromItem<br />index = " + e.fromitem.index + "<br />value = " + value;
		
		value = "";
		if (e.toitem.index > -1) {
			_value = e.toitem.value;
			value = _value.province +  _value.city +  _value.district +  _value.street +  _value.business;
		}    
		str += "<br />ToItem<br />index = " + e.toitem.index + "<br />value = " + value;
		G("searchResultPanel").innerHTML = str;
	});

	var myValue;
	ac.addEventListener("onconfirm", function(e) {    
	var _value = e.item.value;
		myValue = _value.province +  _value.city +  _value.district +  _value.street +  _value.business;
		G("searchResultPanel").innerHTML ="onconfirm<br />index = " + e.item.index + "<br />myValue = " + myValue;
		
		setPlace();
	});

	function setPlace(){
		map.clearOverlays();    
		function myFun(){
			var pp = local.getResults().getPoi(0).point;   
			map.centerAndZoom(pp, 18);
			map.addOverlay(new BMap.Marker(pp));    
		}
		var local = new BMap.LocalSearch(map, { 
		  onSearchComplete: myFun
		});
		local.search(myValue);
	}
	
	var size = new BMap.Size(900, 20);
	map.addControl(new BMap.CityListControl({
		anchor: BMAP_ANCHOR_TOP_LEFT,
		offset: size,
	}));
	
	var top_left_control = new BMap.ScaleControl({anchor: BMAP_ANCHOR_TOP_LEFT});
	var top_left_navigation = new BMap.NavigationControl(); 
	var top_right_navigation = new BMap.NavigationControl({anchor: BMAP_ANCHOR_TOP_RIGHT, type: BMAP_NAVIGATION_CONTROL_SMALL});
	map.addControl(top_left_control);
	map.addControl(top_left_navigation);     
	map.addControl(top_right_navigation);  

	function searchwalkRoute(){
		map.clearOverlays();  
		var start=document.getElementById("start").value;
		var destiny=document.getElementById("destiny").value;
		map.clearOverlays();
		var walking = new BMap.WalkingRoute(map, {renderOptions:{map: map, autoViewport: true}});
		walking.search(start,destiny);
	}
	
	
	function searchcarRoute(){
		map.clearOverlays();
		var start2=document.getElementById("start2").value;
		var destiny2=document.getElementById("destiny2").value;
		var routePolicy = [BMAP_DRIVING_POLICY_LEAST_TIME,BMAP_DRIVING_POLICY_LEAST_DISTANCE,BMAP_DRIVING_POLICY_AVOID_HIGHWAYS];
		var i=document.getElementById("driving_way").value;
		search(start2,destiny2,routePolicy[i]); 
		function search(start,end,route){ 
			var driving = new BMap.DrivingRoute(map, {renderOptions:{map: map, autoViewport: true},policy: route});
			driving.search(start,end);
		}
	}
</script>
