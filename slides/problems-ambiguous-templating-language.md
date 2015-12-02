## Ambiguous Templating Language

```html
    <div ng-repeat="model in collection">
        <input 
            ng-model="model.name" 
            ng-click="model.doSomething()" 
            typeahead="true"
            placeholder="notBoundButCanBeUsed"
            ng-attr-placehoder="{{model.suggestion}}" />
    </div>
```
