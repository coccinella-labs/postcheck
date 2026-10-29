# postcheck

Pre-post validation guard for GitHub comments and posts.

## What it checks

1. **Em dashes (U+2014)** - Rejects text containing the em dash character.
2. **Unpaired backticks** - Rejects text with an odd number of backticks after removing escaped backticks.

## Usage

```bash
echo "some text" | postcheck
postcheck < file_to_check
cat file | postcheck
```

## Exit codes

- `0` - text is clean, safe to post
- `1` - issue detected, do not post

## Installation

```bash
ln -s /path/to/postcheck /usr/local/bin/postcheck
```
