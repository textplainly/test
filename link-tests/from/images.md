# image emebed link tests

## relative

| path                  | test                                                                                             |
|-----------------------|--------------------------------------------------------------------------------------------------|
| `making a list.jpg`   | <img src="making a list.jpg"><p>Dear Karma, I have a list of people you missed.</p>              |
| `../spanky.gif`       | <img src="../spanky.gif"><p>I hope karma slaps you in the face before I do</p>                   |
| `../to/grrrr.gif`     | <img src="../to/grrrr.gif"><p>How people treat you is their karma; How you react is yours...</p> |
| `../to/what?.gif`[^1] | <img src="../to/what?.gif">                                                                      |
| `../to/what%3F.gif`   | <img src="../to/what%3F.gif">                                                                    |

## absolute

| path                                 | test                                                                                                      |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `/link-tests/from/making a list.jpg` | <img src="/link-tests/from/making a list.jpg"><p>Dear Karma, I have a list of people you missed.</p>      |
| `/link-tests/spanky.gif`             | <img src="/link-tests/spanky.gif"><p>I hope karma slaps you in the face before I do</p>                   |
| `/link-tests/to/grrrr.gif`           | <img src="/link-tests/to/grrrr.gif"><p>How people treat you is their karma; How you react is yours...</p> |
| `/link-tests/to/what?.gif`[^1]       | <img src="/link-tests/to/what?.gif">                                                                      |
| `/link-tests/to/what%3F.gif`         | <img src="/link-tests/to/what%3F.gif">                                                                    |

Links back to start:

[`start.md`](start.md)

[`./start.md`](./start.md)

[^1]: GitHub.com fails to handle the `?`, requiring it to be escaped as in the next row.
