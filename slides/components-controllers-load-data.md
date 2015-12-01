##  Controllers load data
- New router doesn't have a resolve state
- Controllers need to trigger it
- Delegate to data stores in constructor

```javascript
/*@ngInject*/
export class MessagesComponent {
    constructor(messageStore) {
        messageStore.fetchAll()
            .then(messages => this.messages = messages);
    }
}
```
