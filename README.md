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
| `metrics`, `snippet`, `note` | optional card extras (real data only) |
| `sources` | list of `kind`/`ref`/`url`/`note`, shown at the end of a post |

## Status page

`data/status.yaml` drives `/status/`. It ships with sample data. Replace it with verified facts only.

## Theme

Design tokens come from `design/DESIGN.md` (Google Stitch). The theme lives in its own repo, [m0hss/hugo-fixlog](https://github.com/m0hss/hugo-fixlog) (MIT), included here as a git submodule at `themes/fixlog/`. After cloning, run `git submodule update --init`.
