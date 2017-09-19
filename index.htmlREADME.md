# Angularjs
<!DOCTYPE html>
<html>
	<head>
		<title>Angularjs</title>
		<link rel = "stylesheet" href = "style.css">
		<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.4/angular.min.js"></script>
		<script src = "script.js"></script>
	</head>
	<body>
	<div ng-app = "myapp" ng-controller = "mycont">
		<label>Search <input ng-model = "search">
		Show:<select ng-model = "select" class = "form-control">
			<option value = "5">5</option>
			<option value = "10">10</option>
			<option value = "15">15</option>
		</select>
		<br></br>
		<table>
		<tr>
			<th ng-click = "sort('EmployeeName')">Employee Name</th>
			<th ng-click = "sort('Employeedep')">Employee Department</th>
			<th>Role</th>
			<th>Mobile Number</th>
		</tr>
		<tr ng-repeat = "members in member | orderBy : myorder | filter : search | filter : select">
			<td>{{members.EmployeeName}}</td>
			<td>{{members.Employeedep}}</td>
			<td>{{members.Role}}</td>
			<td>{{members.MobileNumber}}</td>
		</table>
	</div>
</html>
