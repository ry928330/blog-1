### Roadmap

[roadmap](https://github.com/Microsoft/TypeScript/wiki/Roadmap)

### 3.7

#### Optional Chaining Operator(可选链操作符)

Optional Chaining Operator can help us `reduce some code` when we judge `foo.bar.baz` as follow:

```js
// Before
if (foo && foo.bar && foo.bar.baz) {
  // ...
}

// After-ish
if (foo?.bar?.baz) {
  // ...
}
```

`?:`: check in `undefined` and `null`.

```js
undefined ?: 1 // undefined
null ?: 1      // undefined
0 ?: 1         // 1
'' ?: 1        // 1
NaN ?: 1       // 1
```

> `&&` has different behaviour. Not only `undefined` and `null`, but `falsy value` will be also checked. eg:

```js
undefined && 1 // undefined
null && 1      // null
0 && 1         // 0
'' && 1        // ''
NaN && 1       // NaN
```

#### Nullish Coalescing Operator(空值合并操作符)

`??` means you can take the value that isn't `undefined` or `null`.

```js
undefined ?? 1 // 1
null ?? 1      // 1
0 ?? 1         // 0
'' ?? 1        // ''
```

> `||` has different behaviour. Not only `undefined` and `null`, but `falsy value` will be also checked. eg:

```js
undefined || 1 // 1
null || 1      // 1
0 || 1         // 1
'' || 1        // 1
```