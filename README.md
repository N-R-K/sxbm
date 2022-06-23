# sxbm

[![CodeBerg](https://img.shields.io/badge/Hosted_at-Codeberg-%232185D0?style=flat-square&logo=CodeBerg)](https://codeberg.org/NRK/sxbm)

I needed a simple and browser-independent way of managing my bookmarks, leading to the creation of sxbm.
It's written in strictly POSIX compliant shell, so it should work fine on all \*nix based operating system.

Sxbm stores your bookmarks in a plain text file making it easily portable.
Bookmarks are categorized via tags as opposed to the inferior folder structure found in browsers.

## Installation

Cone the repo.
```
git clone https://codeberg.org/NRK/sxbm.git
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

Edit bookmarks.
```
sxbm edit
```

Remove a bookmark.
```
sxbm rm <line_number>
```

Run `sxbm --help` to see more detailed usage.

## Searching

Searching by tag
```
sxbm ls +tag
```

Searching by title
```
sxbm ls title
```

By default tag searches are non-strict while title searches are strict.

In other words, `sxbm ls +one +two` will match bookmarks that have EITHER
`+one` OR `+two`. If you wish to search for a bookmark that contains ALL the
specified tags then you can pass the `-s` or `--strict` option.
e.g `sxbm ls -s +one +two +three` will only match bookmarks that have all three
of the tags.

As for titles, `sxbm ls aplha beta` will match bookmarks that contains BOTH
`alpha` and `beta`. You can pass the `-S` option to search for entries that
contain either one of the queries.

One more thing to keep in mind is that title search also matches links. The
rational is that you may want to search `sxbm ls "gentoo.org"` to find
bookmarks with the specified url.

## Using it with Dmenu/Rofi

There's an example wrapper [script](extra/sxbm_dmenu) provided which allows you
to open, copy and add bookmarks via dmenu/rofi.

## Todo

- [ ] Enhance `remove` arguments. Should take same arguments as `open`.
- [ ] Enhance `edit` arguments. Should take similar arguments as `open`.
- [ ] Add PGP encryption.
