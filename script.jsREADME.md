# Angularjs
angular.module('myapp',[])
	.controller('mycont',
		function($scope,$http){
			$http.get('https://api.myjson.com/bins/7xp8d').then(function(response){
			$scope.member = response.data;
			},function(error){
				console.log(error);
			});
			$scope.sort = function(members){
				$scope.myorder = members;
			}
		}
	)
	// myapp.filter('startFrom', function() {
    // return function(input, start) {
        // start = +start; //parse to int
        // return input.slice(start);
    // }
// });
