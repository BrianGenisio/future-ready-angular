## Use Classes
- Idiomatic Angular 2 code uses classes

```javascript
/*@ngInject*/
class MessageStore extends EventEmitter {
    constructor(runtime, dependencies) {
        this.runtime = runtime;
        this.dependencies = dependencies;
    }

    get messages() {
        return this.cachedMessages;
    }

    getAll() {
        return fetch('api/call')
            .then(data => this.cachedMessages = data);
    }
}
```