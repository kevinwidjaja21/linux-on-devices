Below are my edit to `sxmobar_hook_statusbar.sh` to work around the rounded edge and notch. Note that sway ui scaling of 2.6 is used. This works by using empy character `‎` instead of whitespace.

```bash
sxmobar -a edge 100 " ‎ ‎"
sxmobar -a notch 35 " ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎"
```