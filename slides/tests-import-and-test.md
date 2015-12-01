##  Just Import and Test

```javascript
import {MessagesStore} from '../app/stores/messages';

const test = {};

describe('MessagesStore', () => {
  beforeEach(() => test.subject = new MessagesStore());

  describe('retrieval', () => {
    it('gets all the messages', done => {
      test.subject.fetchAll()
        .then(messages => {
          expect(messages.length).toBe(0);
          done();
         });
    });
  });
});
```