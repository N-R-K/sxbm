# sxbm
Simple Unix Bookmark Manager, a posix compliant shell script for managing your bookmarks.

The script stores your bookmarks on a plain text file making it easily portable.

## Installation and Usage
Cone the repo.

```
git clone https://github.com/N-R-K/sxbm.git
```

Then just copy/move the script into your $PATH.
Instead of copying, you can also create a symlink. This way you can do a git pull to get updates.

## Usage
Adding a bookmark (title and tag are optional.)
```
sxbm add link.com title +tag
```

Opening a bookmark. You need to specify a title, tag or line_number. If there are multiple results use `sxbm open -f` to open them all.
```
sxbm open <title|+tag|line_number>
```

List all bookmarks.
```
sxbm ls
```

You can also list bookmarks by title or tags.
```
sxbm ls title
sxbm ls +tag
```

Edit bookmarks.
```
sxbm edit
```

Run `sxbm --help` to see more detailed usage.

## Todo

- [ ] Implement remove. Should take same arguments as `open`.
- [ ] Enhance `edit` arguments. Should take similar arguments as `open`.
- [ ] Add a dmenu/rofi wrapper.
- [ ] Add PGP encryption.
