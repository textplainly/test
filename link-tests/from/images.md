# image emebed link tests

## relative

| path                    | test                              |
|-------------------------|-----------------------------------|
| `making a list.jpg`      | <img src="making a list.jpg"><br>Dear Karma, I have a list of people you missed.     |
| `../spanky.gif` | <img src="../spanky.gif"><br>I hope karma slaps you in the face before I do |
| `../to/grrrr.gif`      | <img src="../to/grrrr.gif"><br>How people treat you is their karma; How you react is yours...     |
| `../to/what?.gif`      | <img src="../to/what?.gif"> |

## absolute

| path                    | test                              |
|-------------------------|-----------------------------------|
| `/link-tests/from/making a list.jpg`      | <img src="/link-tests/from/making a list.jpg"><br>Dear Karma, I have a list of people you missed.     |
| `/link-tests/spanky.gif` | <img src="/link-tests/spanky.gif"><br>I hope karma slaps you in the face before I do |
| `/link-tests/to/grrrr.gif`      | <img src="/link-tests/to/grrrr.gif"><br>How people treat you is their karma; How you react is yours...     |
| `/link-tests/to/what?.gif`      | <img src="/link-tests/to/what?.gif"> |

Links back to start:

[`start.md`](start.md)

[`./start.md`](./start.md)
