# agreement-exhibits-decimal-numbering
decimal numbering for agreements with exhibits

# Tests

```javascript
var assert = require('assert')
var aed = require('agreement-exhibits-decimal-numbering')

assert.equal(
  aed(
    [ { series:  { number: 1, of: 1 },
        element: { number: 1, of: 1 } },
      { series:  { number: 1, of: 1 },
        element: { number: 1, of: 1 } },
      { series:  { number: 1, of: 1 },
        element: { number: 2, of: 2 } } ]),
  'Section 1.2 of the Agreement')

assert.equal(
  aed(
    [ { series:  { number: 1, of: 1 },
        element: { number: 2, of: 2 } },
      { series:  { number: 1, of: 1 },
        element: { number: 1, of: 1 } },
      { series:  { number: 1, of: 1 },
        element: { number: 2, of: 2 } },
      { series:  { number: 1, of: 1 },
        element: { number: 3, of: 3 } } ]),
  'Section 1.2.3 of Exhibit 1')
```
