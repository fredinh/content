---
title: Int32Array() constructor
slug: Web/JavaScript/Reference/Global_Objects/Int32Array/Int32Array
tags:
  - Constructor
  - JavaScript
  - Reference
  - TypedArrays
  - Polyfill
browser-compat: javascript.builtins.Int32Array.Int32Array
---
{{JSRef}}

The **`Int32Array()`** typed array constructor creates an array
of twos-complement 32-bit signed integers in the platform byte order. If control over
byte order is needed, use {{jsxref("DataView")}} instead. The contents are initialized
to `0`. Once established, you can reference elements in the array using the
object's methods, or using standard array index syntax (that is, using bracket
notation).

## Syntax

```js
new Int32Array(); // new in ES2017
new Int32Array(length);
new Int32Array(typedArray);
new Int32Array(object);
new Int32Array(buffer);
new Int32Array(buffer, byteOffset);
new Int32Array(buffer, byteOffset, length);
```

### Parameters

- `length`
  - : When called with a `length` argument, an internal array buffer
    is created in memory, of size `length` _multiplied by
    `BYTES_PER_ELEMENT`_ bytes, containing zeros.
- `typedArray`
  - : When called with a `typedArray` argument, which can be an object of any
    of the **non**-{{glossary("bigint")}} typed-array types (such as `Int32Array`), the
    `typedArray` gets copied into a new typed array. Each value in
    `typedArray` is converted to the corresponding type of the
    constructor before being copied into the new array. The length of the new typed array
    will be same as the length of the `typedArray` argument.
- `object`
  - : When called with an `object` argument, a new typed array is
    created as if by the `TypedArray.from()` method.
- `buffer`, `byteOffset`,
  `length`
  - : When called with a `buffer`, and optionally a
    `byteOffset` and a `length` argument, a
    new typed array view is created that views the specified {{jsxref("ArrayBuffer")}}.
    The `byteOffset` and `length` parameters
    specify the memory range that will be exposed by the typed array view. If both are
    omitted, all of `buffer` is viewed; if only
    `length` is omitted, the remainder of
    `buffer` is viewed.

## Examples

### Different ways to create an Int32Array

```js
// From a length
const int32 = new Int32Array(2);
int32[0] = 42;
console.log(int32[0]); // 42
console.log(int32.length); // 2
console.log(int32.BYTES_PER_ELEMENT); // 4

// From an array
const arr = new Int32Array([21,31]);
console.log(arr[1]); // 31

// From another TypedArray
let x = new Int32Array([21, 31]);
const y = new Int32Array(x);
console.log(y[0]); // 21

// From an ArrayBuffer
const buffer = new ArrayBuffer(16);
const z = new Int32Array(buffer, 0, 4);

// From an iterable
const iterable = function*(){ yield* [1,2,3]; }();
const int32_from_iterable = new Int32Array(iterable);
// Int32Array[1, 2, 3]
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

### Compatibility notes

Starting with ECMAScript 2015, `Int32Array` constructors require to be
constructed with a {{jsxref("Operators/new", "new")}} operator. Calling a
`Int32Array` constructor as a function without `new`, will throw a
{{jsxref("TypeError")}} from now on.

```js example-bad
const dv = Int32Array([1, 2, 3]);
// TypeError: calling a builtin Int32Array constructor
// without new is forbidden
```

```js example-good
const dv = new Int32Array([1, 2, 3]);
```

## See also

- [Polyfill of `Int32Array` in `core-js`](https://github.com/zloirock/core-js#ecmascript-typed-arrays)
- [JavaScript typed arrays](/en-US/docs/Web/JavaScript/Typed_arrays)
- {{jsxref("ArrayBuffer")}}
- {{jsxref("DataView")}}
