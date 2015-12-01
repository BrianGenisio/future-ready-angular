## Hello Components

- Like Web Components <!-- .element: class="fragment" -->
- Most views and directives will be Components <!-- .element: class="fragment" -->
- HTML, JavaScript, CSS, Assets <!-- .element: class="fragment" -->

```javascript
@Component({
    selector: 'person',
    template: `
    <div>
        <span class="first-name">{{model.first}}</span>
        <span class="last-name">{{model.last}}</span>
    </div>
`
})
export class PersonView {
    @Input() model;
    @Output() upVote = new EventEmitter();
}
```
