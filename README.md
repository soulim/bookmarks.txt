# bookmarks.txt

bookmarks.txt is a concept of keeping bookmarks in plain text files.

## Principals

- Bookmark URLs are stored in files named `bookmarks.txt`. The format is described below.
- A "global" bookmarks file is located in the home directory (`$HOME/bookmarks.txt`).
- "Local" bookmarks files could exist in different directories as well.

## Format

URLs are stored one per line without leading and trailing space characters.

Example:

```
https://www.example.com
https://sul.im
```

## Tools

The plain text nature of bookmark files allows to use any program to manage URLs.The `bin/` directory of this repository contains `bookmarks` script that could be used to list existing and add new URLs. However nothing should stop you from building your own tools.

## Usage

Use [fzf] to select a URL and open it in the default browser:

```ShellSession
$ ./bin/bookmarks | fzf | xargs open
```

Add a new URL:

```ShellSession
$ ./bin/bookmarks https://github.com/soulim/bookmarks.txt
```

## Contributing

bookmarks.txt is open to code contributions for bug fixes only. As features might carry a long-term maintenance burden, they will not be accepted at this time. Please submit an issue if you have a feature you would like to request.

## License

See [LICENSE](LICENSE) for license text.


[fzf]: https://github.com/junegunn/fzf
