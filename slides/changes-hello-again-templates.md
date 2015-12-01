## Hello Again Templates

```html
    <div *ng-for="#model of collection">
        <input 
            [(ng-model)]="model.name" 
            (click)="model.doSomething()" 
            [typeahead]="true"
            [placehoder]="model.suggestion" />
    </div>
```