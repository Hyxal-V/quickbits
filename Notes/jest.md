# Jest 
Testing Framework for Javascript


#### Test Functions

| Function                          | Purpose                          |
|----------------------------------|----------------------------------|
| `test(name, fn)`                 | Define a test                    |
| `it(name, fn)`                   | Alias for `test`                 |
| `describe(name, fn)`             | Group related tests              |
| `beforeEach(fn)` / `afterEach(fn)` | Setup/teardown per test        |
| `beforeAll(fn)` / `afterAll(fn)`   | Setup/teardown once per suite  |

### Basic Usage
```js
const sum = (a, b) => a + b;
test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3);
});

```

### Matchers
----
```js
expect(value).toBe(expected);       // primitive equality
expect(value).toEqual(obj);         // deep equality
expect(fn).toThrow();               // error thrown
expect(arr).toContain(item);        // contains item
expect(val).toBeTruthy();           // truthy
expect(val).toBeFalsy();            // falsy
```