---
title: File()
slug: Web/API/File/File
page-type: web-api-constructor
tags:
  - API
  - Constructor
  - File API
  - Reference
browser-compat: api.File.File
---
{{APIRef("File")}}

The **`File()`** constructor creates a new {{domxref("File")}}
object instance.

## Syntax

```js
new File(bits, name
new File(bits, name, options)
```

### Parameters

- `bits`
  - : An {{jsxref("Array")}} of {{jsxref("ArrayBuffer")}}, {{domxref("ArrayBufferView")}},
    {{domxref("Blob")}}, string objects, or a mix of any of such
    objects, that will be put inside the {{domxref("File")}}.
    Note that strings objects here are encoded as UTF-8, unlike the usual JS UTF-16 strings.
- `name`
  - : A string representing the file name or the path to the file.
- `options` {{optional_inline}}

  - : An options object containing optional attributes for the file. Available options are
    as follows:

    - `type`
      - : A string representing the MIME type of the
        content that will be put into the file. Defaults to a value of `"".`
    - `lastModified`
      - : A number representing the number of milliseconds
        between the Unix time epoch and when the file was last modified. Defaults to a
        value of {{jsxref("Date.now()")}}.

## Examples

```js
const file = new File(["foo"], "foo.txt", {
  type: "text/plain",
});
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{domxref("FileReader")}}
- {{domxref("Blob")}}
