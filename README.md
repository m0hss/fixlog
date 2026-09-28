# Fixlog

Sassi's personal, unofficial dev log. Built with [Hugo](https://gohugo.io) (extended, v0.146+).
Not affiliated with FixByte.

## Run it

```bash
hugo server          # http://localhost:1313
hugo --minify        # builds to public/
hugo new posts/my-experiment.md
```

## Writing a post

Front matter fields the theme uses:

| field     | values                                          |
|-----------|-------------------------------------------------|
| `outcome` | `worked`, `failed`, `in-progress`, `poking`     |
| `tags`    | list of tags                                    |
| `summary` | one-line hook shown on cards                    |

## Status page

`data/status.yaml` drives `/status/`. It ships with sample data. Replace it with verified facts only.

## Theme

The theme lives in `themes/fixlog/` and is self-contained (MIT) so it can be published on its own later.
