# sxbm-dmenu

This is a small example dmenu wrapper around sxbm. Feel free to customize/tweak
it to your needs.

By default `sxbm_dmenu` takes the exact same arguments as `sxbm ls`. Invoking
`sxbm_dmenu` without any argument will list out all the bookmarks in your
`$prompt` (dmenu by default) and will open that link via `sxbm open`.

To list matching titles: `sxbm_dmenu title`
To list matching tags: `sxbm_dmenu +tag`

* Additional arguments: `sxbm_dmenu` takes two additional arguments.

    * `-y` or `--yank` will copy the selected link to your clipboard
      (requires `xclip`) instead of opening them. Example: `sxbm_dmenu -y title`

    * `-a` or `--add` is an alias to `sxbm add`.
      Example: `sxbm_dmenu -a link.com +tag`

