# CHANGELOG

> Package changelog.

<section class="release" id="v0.1.1">

## 0.1.1 (2024-07-26)

No changes reported for this release.

</section>

<!-- /.release -->

<section class="release" id="v0.1.0">

## 0.1.0 (2024-04-13)

<section class="features">

### Features

-   [`ec1c506`](https://github.com/stdlib-js/stdlib/commit/ec1c5066955fdcc71013805a5c55fc739d29a849) - resolve negative index arguments relative to last index
-   [`58bdac8`](https://github.com/stdlib-js/stdlib/commit/58bdac8a8a5914b7b2598f873418f9edae4c8843) - add `string/base/replace-after-last` [(##1365)](#1365)

</section>

<!-- /.features -->

<section class="breaking-changes">

### BREAKING CHANGES

-   [`ec1c506`](https://github.com/stdlib-js/stdlib/commit/ec1c5066955fdcc71013805a5c55fc739d29a849): resolve negative index arguments relative to last index
-   [`ec1c506`](https://github.com/stdlib-js/stdlib/commit/ec1c5066955fdcc71013805a5c55fc739d29a849): resolve negative index arguments relative to last index 

    -   Previously, a negative `fromIndex` argument would resolve to `0`.
    The current behavior resolves relative to the last character index.
    To preserve the previous behavior, users should clamp index arguments
    to index bounds before calling `replaceAfterLast`.

</section>

<!-- /.breaking-changes -->

<section class="issues">

### Closed Issues

This release closes the following issue:

[##814](#814)

</section>

<!-- /.issues -->

<section class="commits">

### Commits

<details>

-   [`ec1c506`](https://github.com/stdlib-js/stdlib/commit/ec1c5066955fdcc71013805a5c55fc739d29a849) - **feat:** resolve negative index arguments relative to last index _(by Athan Reines)_
-   [`58bdac8`](https://github.com/stdlib-js/stdlib/commit/58bdac8a8a5914b7b2598f873418f9edae4c8843) - **feat:** add `string/base/replace-after-last` [(##1365)](#1365) _(by Golden Kumar, Athan Reines, Philipp Burckhardt)_

</details>

</section>

<!-- /.commits -->

<section class="contributors">

### Contributors

A total of 3 people contributed to this release. Thank you to the following contributors:

-   Athan Reines
-   Golden Kumar
-   Philipp Burckhardt

</section>

<!-- /.contributors -->

</section>

<!-- /.release -->

