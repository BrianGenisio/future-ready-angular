## ControllerAs directives
- Define directives using <!-- .element: class="fragment" --> `controllerAs` <!-- .element: class="fragment" -->
- Use Angular 1.4 <!-- .element: class="fragment" -->
- Reference the VM in the template <!-- .element: class="fragment" -->

```javascript
module.directive('myComponent', function() {
    return {
        template,
        controllerAs: 'vm',
        bindToController: { text: '@', data: '=', action: '&' },
        controller: MyComponentController
    };
});

export class MyComponentController {
    doSomething() {
        alert('something');
    }
}
```

```html
<button ng-click="vm.doSomething()" />
```
