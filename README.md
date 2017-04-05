# style
Personal styleguides.

## Javascript

### Function Declarations

- space between `function` and the identifier
- no space between the identifier and the argument list
- arguments delimited by `, `
- curly brace on same line

Single-Line:

```js
function f(x, y, z) {

}
```

Multiline:
```js
function f(
	very_long_argument_1,
	very_long_argument_2,
	very_long_argument_3
) {

}
```

### Object Literals

- space between braces, key/colon pairs, and values

Single-Line:

```js
const obj = { a: 1, b: 2, c: { d: 3 } }
```

Multiline:

```js
const obj = {
	a: 1,
	b: 2,
	c: {
		d: 3
	}
}
```

### Array Literals

- elements delimited by `, `

Single-Line:

```js
const arr = [1, 2, 3, 4, 5]
```

Multiline:

```js
const arr = [
	1,
	2,
	3,
	4,
	5
]
```

### Conditionals

- space between `if` and conditional

Single-Line:

```js
if (p) f()
```

Multiline:

```js
if (p) {
	f()
}
```

### Ternaries

- space between expressions, `?`, and `:`

Single-Line:

```js
const result = x ? y : z
```

Multiline:

```js
const result = x
	? y
	: z
```

Else-If Chain:

```js
const result =
	p1 ? a :
	p2 ? b :
	p3 ? c :
	d
```

Conditional Tree:

```js
const result =
	p1
		? p2
			? a
			: b
		: p3
			? c
			: d
```

### Callbacks

Single-Line:

```js
arr.map(x => x + 1)
```

Multiline:

```js
fs.readdir('.', (err, files) => {
	if (err) return handle_error(err)
	// ...
})
```

### Casing

Constants use `UPPER_SNAKE_CASE`
Variables and functions use `lower_snake_case`
String identifiers use `lower-kebab-case`

```
const SOME_CONSTANT = 42

const some_variable = some_function(x)

const package_name = 'some-package'
```

### Nullable Values

Values with `Maybe` semantics should always be either the value or `null`. Don't use `undefined` (it's not a function).

### Indentation

Use hard tabs with four spaces.

### Semicolons

Only use semicolons to delimit multiline expressions or in a for-loop.

```js
;(1 + 2).toString()
;[1, 2, 3].forEach(console.log)
for (;;) {
	// ...
}
```

### Special Cases

When a multiline function call contains only object/array literals or when an array literal contains only object literals, the child constructions can be collapsed one indentation level into the parent construction.

```js
f({
	a: 1
}, {
	b: 2
}, [
	1,
	2,
	3,
	4
])

const arr = [{
	a: 1
}, {
	b: 2
}]
```
