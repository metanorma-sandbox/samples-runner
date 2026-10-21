# samples-runner

Runs long metanorma sample/corpus jobs (`mn-samples-*`) on the
`metanorma-sandbox` org's runner quota, without transferring any repo.

Dispatch **run** with:

| Input | Meaning |
|---|---|
| `repo` | short name under `metanorma/` (e.g. `mn-samples-iso`) |
| `ref` | ref to run (default `main`) |
| `command` | shell command executed in the repo root |
| `bundle_install` | run a fresh `bundle install` first (default true) |
| `ruby_version` | default `3.3` |

Jobs get up to 6 hours. The metanorma-ci PAT is used for private
checkouts and submodules only; the job never pushes.
