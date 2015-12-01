## Treat app.js like a DI container
- Keep injectables as PoJos <!-- .element: class="fragment" -->
- Create a bootstrapping in the main app <!-- .element: class="fragment" -->

```javascript
import {MailboxStore} from '../stores/mailbox';
import {UserStore} from '../stores/user';
import {SettingsStore} from '../stores/settings';

angular
  .module('app', [
    routes,
    mainModule
  ])
  .factory('mailboxStore', () => new MailboxStore())
  .factory('userStore', () => new UserStore())
  .factory('settingsStore', () => new SettingsStore())
```
