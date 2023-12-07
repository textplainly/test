# link tests start here

## links to `to/finish.md`

[`../to/finish.md`](../to/finish.md)

[`/link-tests/to/finish.md`](/link-tests/to/finish.md)


## links to `to/what?.md`

[`../to/what?.md`](../to/what?.md)

[`/link-tests/to/what?.md`](/link-tests/to/what?.md)


## links to `to` directory

[`../to`](../to)

[`../to/`](../to/)

[`/link-tests/to`](/link-tests/to)

[`../to/README.md`](../to/README.md)


## links to current directory

[`.`](.)

[`/link-tests/from`](/link-tests/from)


## links to sibling

[`images.md`](images.md)

[`./images.md`](./images.md)


## links to parent directory

[`..`](..)

[`/link-tests`](/link-tests)

[`../README.md`](../README.md)


## links to root directory

[`../..`](../..)

[`/`](/)

[`../../README.md`](../../README.md)


## links to source code

[`start.js`](start.js)

[`../to/finish.js`](../to/finish.js)


## ⚠️ invalid links

[`to/finish.md`](to/finish.md)

[`/finish.md`](/finish.md)

[`...`](...)

On GitHub.com, the above result in a special 404 page, specifically stating that
the repo branch in question does not contain the given path:

> The master branch of test does not contain the path `link-tests/from/to/finish.md`.

> The master branch of test does not contain the path `finish.md`.

> The master branch of test does not contain the path `link-tests/from/...`.


### links past root directory

Unlike the invalid links above, on GitHub.com, these below result in the
general 404 page shown for all regular invalid GitHub.com GET requests.

[`../../..`](../../..)   `https://github.com/textplainly/test/blob`

[`/..`](/..)

[`../../../..`](../../../..)

[`../../../../..`](../../../../..)

[`../../../../../..`](../../../../../..)
