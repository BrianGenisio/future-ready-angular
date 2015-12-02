## Hello Again Dependency Injection

- No Factories or Services <!-- .element: class="fragment" -->
- No Angular Modules       <!-- .element: class="fragment" -->
- Setup more like a C# DI container <!-- .element: class="fragment" -->

```javascript
bootstrap(AppComponent, [
    provide(PersonStore, {useClass: PersonStore}),
    provide(MailboxStore, {useValue: new MailboxStore()}),
    provide(Chocolate, {useFactory: new ChocolateFactory()})
]);
```
