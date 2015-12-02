## No more $scope
- Avoid passing $scope into controllers <!-- .element: class="fragment" -->
- Avoid passing $rootScope into most code <!-- .element: class="fragment" -->
- Abstract any $scope behavior <!-- .element: class="fragment" -->
- Use EventEmitter for $on, $broadcast, $emit <!-- .element: class="fragment" -->