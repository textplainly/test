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

| path                                           | description                                  | TextAssembly spec | GitHub.com behavior                                                                                                                  |
|------------------------------------------------|----------------------------------------------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [`to/finish.md`](to/finish.md)                 | nonexistent path within assembly             |                   | repo-specific 404 page: *The master branch of test does not contain the path `link-tests/from/to/finish.md`.*                        |
| [`/finish.md`](/finish.md)                     | nonexistent path within assembly             |                   | repo-specific 404 page: *The master branch of test does not contain the path `finish.md`.*                                           |
| [`...`](...)                                   | nonexistent path within assembly             |                   | repo-specific 404 page: *The master branch of test does not contain the path `link-tests/from/...`.*                                 |
| [`/..`](/..)                                   | directory above assembly root                |                   | regular GitHub.com  404 page                                                                                                         |
| [`../../..`](../../..)                         | directory above assembly root                |                   | regular GitHub.com  404 page                                                                                                         |
| [`../../../..`](../../../..)                   | directory *further* above assembly root      |                   | the page for the root of the repo, but to the default or HEAD branch, which in this case is effectively the same as [`../..`](../..) |
| [`../../../../..`](../../../../..)             | directory *even further* above assembly root |                   | the page for the owner of the repo                                                                                                   |
| [`../../../../../..`](../../../../../..)       | ok, this is getting crazy                    |                   | GitHub.com home page                                                                                                                 |
| [`../../../../../../..`](../../../../../../..) | can we stop now?                             |                   | GitHub.com home page                                                                                                                 |

