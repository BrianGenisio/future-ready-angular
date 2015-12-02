## Use Modules
- Stop injecting classes
- Start importing classes

```javascript
export class Message {
    constructor(to, from, subject) {
        this.to = to;
        this.from = from;
        this.subject = subject;
    }

    addMessage(message) {
        this.message = message;
    }
}
```

```javascript
import {Message} from '../models/message';

export class MessageStore {
    createMessage(to, from, subject, body) {
        let result = new Message(to, from, subject);
        result.addMessage(message);
        return result;
    }
}
```
