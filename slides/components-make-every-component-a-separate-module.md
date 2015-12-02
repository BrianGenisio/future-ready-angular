##  Make every component a separate module

```javascript
export const messageViewModule =
    angular.
        .module('component:message-view', [])
        .directive('message', function() { ... })
        .name;

export class MessageView {
}
```

```javascript
import {messageViewModule} from '../message-view';

export const mainViewModule =
    angular.
        .module('component:main-view', [messageViewModule])
        .directive('main', function() { ... })
        .name;
```
