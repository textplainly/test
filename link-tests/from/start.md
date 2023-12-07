# link tests start here

## links to `to/finish.md`

[`../to/finish.md`](../to/finish.md)

[`/link-tests/to/finish.md`](/link-tests/to/finish.md)


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

## links to files with "special" characters in their name


| path                                       | description   | TextAssembly spec | GitHub.com behavior                                          |
| ------------------------------------------ | ------------- | ----------------- | ------------------------------------------------------------ |
| [`../to/zen koans.md`](../to/zen koans.md) | space in name |                   |                                                              |
| [`../to/zen#koans.md`](../to/zen#koans.md) | `#` in name   |                   | links to file named `zen`, but not to the `koans.md` heading within since `zen` is not recognized as a Markdown file. |
| [`../to/what?.md`](../to/zen?.md)          | `?` in name   |                   | repo-specific 404 page: *The master branch of test does not contain the path `link-tests/to/what`.* |



### Analysis

GitHub.com applies URL semantics to all reference paths.

In the case of `?`, it interprets it as delimiting the end of the file path segment and
the start of query parameters, resulting in the following
404 message.

In the case of `#`, it interprets it as delimiting the end of the file path segment and the start of a fragment identifier, a deep link reference within the file.



Should the `#koans.md` at the end of `zen#koans.md` be treated as a link
to the heading `koans.md` in a file named `zen`, or as a link to a file
named `zen#koans.md`?

Notice `?.md` is not included as part of the path in the error message.

TextAssembly, on the other hand, applies Posix semantics to all reference
paths. While a TextAssembly can be *rendered* for the web, in which case references will be converted into URL-compatible form, the TextAssembly
source is *not* web or internet-specific. A TextAssembly behaves essentially
like a self-contained Posix file system volume, where the only characters
not allowed in a file name are `null` and `/`. A TextAssembly principle is that
no paths need escaping, whether they contain spaces or characters like `?` or
`#`.

TextAssembly does give one additional character *potential* special semantics: `#` as a delimiter between a file reference and to a deep reference within that file. We say "potential" because the interpretation
is flexible and dynamic, matching whichever interpretation results in a valid link. For example, a `zen#koans.md` reference would link to a file with that name if it existed, and to the heading `koans.md` within a file named `zen` if that existed. It is highly unlikely that both would
  exist, but if they do the filename match takes precedence over the deep
  link match.


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

