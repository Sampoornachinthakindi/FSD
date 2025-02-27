<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Angular JS Example</title>
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.8.2/angular.min.js"></script>
</head>
<body ng-app="myApp" ng-controller="MainController">
    <h1>{{title}}</h1>
    <input type="text" ng-model="username" placeholder="Enter your name">
    <button ng-click="greetUser()">Great</button>
    <p>{{greetingMessage}}</p>

    <script>
        var app = angular.module('myApp', []);
        app.controller('MainController', function($scope) {
            $scope.title = "Welcome!";
            $scope.greetUser = function() {
                $scope.greetingMessage = $scope.username ? 
                    "Hello, " + $scope.username : 
                    "Please enter your name.";
            };
        });
    </script>
    
</body>
</html>
