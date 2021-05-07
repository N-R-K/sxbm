# sxbm
I needed a simple and browser-independent way of managing my bookmarks, leading to the creation of sxbm.
It's written in strictly POSIX compliant shell, so it should work fine on all \*nix based operating system.

Sxbm stores your bookmarks in a plain text file making it easily portable.
Bookmarks are categorized via tags as opposed to the inferior folder structure found in browsers.

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

Opening a bookmark. You need to specify a title, tag or line\_number.
If there are multiple results use `sxbm open -f` to open them all.
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
