<!--

@license Apache-2.0

Copyright (c) 2025 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# DataType

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Data type constructor.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import DataType from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-dtype-ctor@deno/mod.js';
```

#### DataType( value\[, options] )

Returns a data type instance.

```javascript
var dt = new DataType( 'float64' );
// returns <DataType>
```

The constructor supports the following parameters:

-   **value**: data type value. Must be either a supported [data type][@stdlib/ndarray/dtypes] string, a [struct][@stdlib/dstructs/struct] constructor, or another data type instance.
-   **options**: constructor options (_optional_).

The constructor supports the following options:

-   **description**: data type description.

* * *

## Properties

#### DataType.prototype.alignment

Alignment (in bytes) for the data type.

```javascript
var dt = new DataType( 'float64' );
// returns <DataType>

var v = dt.alignment;
// returns 8
```

If a data type does not have a known alignment, the returned value is `-1`.

#### DataType.prototype.byteLength

Size (in bytes) for the data type.

```javascript
var dt = new DataType( 'float64' );
// returns <DataType>

var v = dt.byteLength;
// returns 8
```

If a data type does not have a known size, the returned value is `-1`.

#### DataType.prototype.byteOrder

Data type byte order.

```javascript
var dt = new DataType( 'float64' );
// returns <DataType>

var v = dt.byteOrder;
// returns 'host'
```

The byte order may be one of the following values:

-   **host**: host platform byte order.
-   **little-endian**: little-endian byte order.
-   **big-endian**: big-endian byte order.

#### DataType.prototype.char

Single letter character abbreviation for the data type.

```javascript
var dt = new DataType( 'float64' );
// returns <DataType>

var v = dt.char;
// returns 'd'
```

If a data type does not have a corresponding single letter character abbreviation, the returned value is an empty string.

#### DataType.prototype.description

Data type description.

```javascript
var dt = new DataType( 'float64' );
// returns <DataType>

var v = dt.description;
// returns '...'
```

If a data type does not have an associated description, the returned value is an empty string.

#### DataType.prototype.enum

Enumeration constant for the data type.

```javascript
var dt = new DataType( 'float64' );
// returns <DataType>

var v = dt.enum;
// returns <number>
```

If a data type does not have a corresponding known enumeration constant, the returned value is the enumeration constant for a user-defined data type.

**Note**: enumeration constants should be treated as **opaque** values. One should **not** assume that a data type has a specific enumeration constant value.

#### DataType.prototype.value

Raw (original) data type value.

```javascript
var dt = new DataType( 'float64' );
// returns <DataType>

var v = dt.value;
// returns 'float64'
```

* * *

## Methods

#### DataType.prototype.toJSON()

Returns a [JSON][json] representation of a `DataType` instance.

```javascript
var dt = new DataType( 'float64' );
// returns <DataType>

var o = dt.toJSON();
// e.g., returns { 'type': 'DataType', 'value': 'float64', 'byteOrder': 'host', ... }
```

[`JSON.stringify()`][mdn-json-stringify] implicitly calls this method when stringifying a `DataType` instance.

#### DataType.prototype.toString()

Returns a string representation of a `DataType` instance.

```javascript
var dt = new DataType( 'float64' );
// returns <DataType>

var str = dt.toString();
// returns 'float64'
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

* * *

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
import DataType from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-dtype-ctor@deno/mod.js';

var dt = new DataType( 'complex128' );

console.log( 'type: %s', typeof dt );
// => 'type: object'

console.log( 'alignment: %d', dt.alignment );
// => 'alignment: 8'

console.log( 'byteLength: %d', dt.byteLength );
// => 'byteLength: 16'

console.log( 'byteOrder: %s', dt.byteOrder );
// => 'byteOrder: host'

console.log( 'char: %s', dt.char );
// => 'char: z'

console.log( 'JSON: %s', JSON.stringify( dt ) );
// e.g., => 'JSON: {"type": "DataType","value":"float64","byteOrder":"host",...}'
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/ndarray-dtype-ctor.svg
[npm-url]: https://npmjs.org/package/@stdlib/ndarray-dtype-ctor

[test-image]: https://github.com/stdlib-js/ndarray-dtype-ctor/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/ndarray-dtype-ctor/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/ndarray-dtype-ctor/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/ndarray-dtype-ctor?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/ndarray-dtype-ctor.svg
[dependencies-url]: https://david-dm.org/stdlib-js/ndarray-dtype-ctor/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/ndarray-dtype-ctor/tree/deno
[deno-readme]: https://github.com/stdlib-js/ndarray-dtype-ctor/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/ndarray-dtype-ctor/tree/umd
[umd-readme]: https://github.com/stdlib-js/ndarray-dtype-ctor/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/ndarray-dtype-ctor/tree/esm
[esm-readme]: https://github.com/stdlib-js/ndarray-dtype-ctor/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/ndarray-dtype-ctor/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/ndarray-dtype-ctor/main/LICENSE

[json]: http://www.json.org/

[mdn-json-stringify]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify

[@stdlib/ndarray/dtypes]: https://github.com/stdlib-js/ndarray-dtypes/tree/deno

[@stdlib/dstructs/struct]: https://github.com/stdlib-js/dstructs-struct/tree/deno

</section>

<!-- /.links -->
