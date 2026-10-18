# HANDOFF — MineSweep

**Generated:** 2026-07-21
**Reason:** 76-fun Thelio to System76 for NVMe repair; work continues elsewhere.
**Repo path on origin machine:** /home/paul/go/src/github.com/MineSweep
**Remote:** git@github.com:PaulSnow/MineSweep.git (origin, fetch + push — SSH)

## 1. What this repo is
Authored work in the sense that it is Paul's own repo under his GitHub account — but it is an
empty placeholder, not a project. It contains exactly three tracked files: a GitHub Go
`.gitignore` template, an MIT `LICENSE`, and a `README.md` whose entire content is the single
line `# MineSweep`. There is no source code of any kind. It is a repo that was created and
then never started. It is disposable.

## 2. Current work in flight
None, and none ever was. Clean tree, nothing unpushed. The history is one commit —
`1830c73 Initial commit` (Paul Snow, 2025-08-10) — which is the GitHub repo-creation commit
that lays down the license, the Go gitignore template and a stub README. The Go `.gitignore`
is the only signal of intent: the project was presumably going to be a Go implementation of
Minesweeper, or something named for it. Nothing was written in the eleven months between that
commit and this handoff. This checkout exists because the repo was created on GitHub and
cloned locally in anticipation of work that never began.

## 3. State at handoff
- **Branch:** main (upstream: origin/main — level, 0 ahead / 0 behind)
- **Uncommitted changes:** none — clean tree
- **Unpushed commits:** 0
- **Disposable?** **Yes.** It holds nothing no other copy has. All three files are pushed to
  github.com/PaulSnow/MineSweep, the tree is clean, and there are no untracked or ignored
  files locally. The entire local directory can be reproduced with one `git clone`. Losing it
  costs nothing at all.
- **Recent commits:**
```
1830c73 Initial commit
```

## 4. Claude setup
No Claude configuration in this repo. No `CLAUDE.md`, no `.claude/`, no `.mcp.json`.

## 5. Directives and conventions
There is nothing to build or test — the repo contains no source files, no `go.mod`, no
`Makefile`, no `package.json`, no CI configuration. Any build or test command would fail for
lack of a project.

The only convention recorded is implied by the checked-in `.gitignore`, which is GitHub's
standard **Go** template (ignores `*.exe`, `*.dll`, `*.so`, `*.dylib`, `*.test`, coverage
output, `vendor/`, `go.work`). If work ever starts here, it was intended to be a Go project;
initialize with `go mod init github.com/PaulSnow/MineSweep` and the standard Go toolchain
(`go build ./...`, `go test ./...`) applies.

Licensing convention: **MIT** (`LICENSE` at root).

## 6. Resuming on another machine
**Disposable — do not restore.** Do not copy this directory off the failing disk.

Reason: every byte of it is on GitHub, the tree is clean, and there is no work here to
preserve. Restoring it would carry over an empty scaffold.

If and when the project actually starts:

1. `git clone git@github.com:PaulSnow/MineSweep.git` (or the HTTPS URL — see the credential
   note below).
2. `go mod init github.com/PaulSnow/MineSweep`
3. Write code. Nothing else needs to be recovered.

**What will not transfer:**
- **SSH credentials — this matters here.** `origin` is **SSH** (`git@github.com:...`), and
  `~/.ssh`, `~/.aws` and `~/.gnupg` were deleted on the origin machine. The clone in step 1
  will fail with a permission/publickey error until a new SSH key is generated and added to
  the GitHub account. Alternatively clone over HTTPS
  (`https://github.com/PaulSnow/MineSweep.git`) with a token, or re-point the remote after
  cloning with `git remote set-url origin ...`.
- Commit signing: if commits here were ever meant to be GPG-signed, `~/.gnupg` is gone and
  the signing key must be regenerated and re-registered with GitHub. The single existing
  commit is not signed, so nothing breaks retroactively.
- The absolute path `/home/paul/go/src/github.com/MineSweep` is a GOPATH-style location and
  carries no meaning under modern Go modules — clone anywhere.
