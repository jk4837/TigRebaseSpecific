# TigRebaseSpecific
Git rebase tool for tig

## Prepare
- Put [rebase_specific](rebase_specific) to `/usr/bin` or other dir in environment path
- Add following line to `~/.tigrc`
  >bind main B !rebase_specific %(commit) "%(prompt Enter rebase action if not reword: )"

## Usage
- Select specific commit in main mode of tig
- Press `B (shift+b)` to trigger script
- Enter one of following option:
  - `k|up`   : move commit later(up)
  - `j|down` : move commit earlier(down)
  ---
  - `i`      : interactive
  - `r`      : reword,   use commit, but edit the commit message
  - `e`      : edit,     use commit, but stop for amending
  - `s`      : squash,   use commit, but meld into previous commit
  - `f`      : fixup,    like \"squash\", but discard this commit's log message
  - `drop`   : remove    commit
  ---
  - `c`      : continue, rebase --continue
  - `a`      : abort,    rebase --abort
  - `*`      : help
