<!--

@license Apache-2.0

Copyright (c) 2024 The Stdlib Authors.

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

# replaceAfterLast

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Replace the substring after the last occurrence of a specified search string.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->

<section class="installation">

## Installation

```bash
npm install @stdlib/string-base-replace-after-last
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var replaceAfterLast = require( '@stdlib/string-base-replace-after-last' );
```

#### replaceAfterLast( str, search, replacement, fromIndex )

Replaces the substring after the last occurrence of a specified search string.

```javascript
var str = 'beep boop';
var out = replaceAfterLast( str, ' ', 'loop', str.length );
// returns 'beep loop'

out = replaceAfterLast( str, 'o', 'bar', str.length );
// returns 'beep boobar'
```

To begin searching from a specific index, provide a corresponding `fromIndex` argument.

```javascript
var out = replaceAfterLast( 'beep boop beep', ' ', 'loop', 6 );
// returns 'beep loop'
```

If `fromIndex` is less than zero, the starting index is resolved relative to the last string character, with the last string character corresponding to `fromIndex = -1`.

```javascript
var out = replaceAfterLast( 'beep boop beep', ' ', 'loop', -1 );
// returns 'beep boop loop'
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

## Notes

-   If a search string is not present in a provided string, the function returns the provided string unchanged.
-   If a search string is an empty string, the function returns the provided string unchanged.
-   If `fromIndex` resolves to an index which is less than `0`, the function returns the provided string unchanged.

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var replaceAfterLast = require( '@stdlib/string-base-replace-after-last' );

var str = 'beep boop';
var out = replaceAfterLast( str, 'p', 'see', str.length );
// returns 'beep boopsee'

str = 'Hello World!';
out = replaceAfterLast( str, 'xyz', 'foo', str.length );
// returns 'Hello World!'

str = 'Hello World!';
out = replaceAfterLast( str, '', 'foo', str.length );
// returns 'Hello World!'

str = '';
out = replaceAfterLast( str, 'xyz', 'foo', str.length );
// returns ''

str = 'beep boop beep baz';
out = replaceAfterLast( str, 'beep', 'foo', 5 );
// return 'beepfoo'
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/string-base/replace-after`][@stdlib/string/base/replace-after]</span><span class="delimiter">: </span><span class="description">replace the substring after the first occurrence of a specified search string.</span>
-   <span class="package-name">[`@stdlib/string-base/replace-before-last`][@stdlib/string/base/replace-before-last]</span><span class="delimiter">: </span><span class="description">replace the substring before the last occurrence of a specified search string.</span>
-   <span class="package-name">[`@stdlib/string-base/replace-before`][@stdlib/string/base/replace-before]</span><span class="delimiter">: </span><span class="description">replace the substring before the first occurrence of a specified search string.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

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

[npm-image]: http://img.shields.io/npm/v/@stdlib/string-base-replace-after-last.svg
[npm-url]: https://npmjs.org/package/@stdlib/string-base-replace-after-last

[test-image]: https://github.com/stdlib-js/string-base-replace-after-last/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/string-base-replace-after-last/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/string-base-replace-after-last/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/string-base-replace-after-last?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/string-base-replace-after-last.svg
[dependencies-url]: https://david-dm.org/stdlib-js/string-base-replace-after-last/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/string-base-replace-after-last/tree/deno
[deno-readme]: https://github.com/stdlib-js/string-base-replace-after-last/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/string-base-replace-after-last/tree/umd
[umd-readme]: https://github.com/stdlib-js/string-base-replace-after-last/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/string-base-replace-after-last/tree/esm
[esm-readme]: https://github.com/stdlib-js/string-base-replace-after-last/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/string-base-replace-after-last/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/string-base-replace-after-last/main/LICENSE

<!-- <related-links> -->

[@stdlib/string/base/replace-after]: https://github.com/stdlib-js/string-base-replace-after

[@stdlib/string/base/replace-before-last]: https://github.com/stdlib-js/string-base-replace-before-last

[@stdlib/string/base/replace-before]: https://github.com/stdlib-js/string-base-replace-before

<!-- </related-links> -->

</section>

<!-- /.links -->
