# Angular-JS-Code

This is an example of a shopping list which untilises Angular JS on a webpage. This enables you to add and remove items using simple JS functions.

<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.3/angular.min.js">
  </script>
  <title>JS Bin</title>
</head>
<body ng-app>
  <H1>Shopping List in Angular JS</h1>
  
 
  
  <form ng-submit="items.push(newItem); newItem={}">
    <label>Item name:
     <input ng-model="newItem.name" />
      </label>
        <button type="submit">Add</button>
  </form>
  
  
  
  <h2>Current Items</h2>
  <hr>
  <p ng-hide="!!items.length">There are no items on the list</p>
  
  <ol ng-init="items=[]">
    <li ng-repeat="item in items">
      {{item.name}}
      (<a href="javascript:void(0)" 
          ng-click="items.splice($index)">X</a>)
    </li>
  </ol>
  <hr>
  <br>
  <br>
  <em>Created by Jamie Ajibade 2017</em>
  
</body>
</html>
