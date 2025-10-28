# Not Working Report

## Specs

```
test_release_plz  ❯ uname -a
Linux desktop 6.17.5-arch1-1 #1 SMP PREEMPT_DYNAMIC Thu, 23 Oct 2025 18:49:03 +0000 x86_64 GNU/Linux

test_release_plz  ❯ dist --version
cargo-dist 0.30.0
```

## Workflows

## Steps

### Add Config Files and Workflows

### Commit Code & Push to Master

Once pushed, we have the following output from release_plz action:

```
 2025-10-28T22:06:12.753380Z  INFO using release-plz config file release-plz.toml
2025-10-28T22:06:12.768511Z  INFO downloading packages from cargo registry crates.io
    Updating crates.io index
2025-10-28T22:06:13.119947Z  WARN Package `test_release_plz@*.*.*` not found
2025-10-28T22:06:13.131914Z  INFO determining next version for test_release_plz 0.1.0
2025-10-28T22:06:13.786787Z  INFO test_release_plz: next version is 0.1.0
2025-10-28T22:06:15.548440Z  INFO opened pr: https://github.com/jdeinum/why_isnt_release_plz_working/pull/1
release_pr_output: {"prs":[{"base_branch":"master","head_branch":"release-plz-2025-10-28T22-06-14Z","html_url":"https://github.com/jdeinum/why_isnt_release_plz_working/pull/1","number":1,"releases":[{"package_name":"test_release_plz","version":"0.1.0"}]}]}
-- Running release-plz release --
2025-10-28T22:06:16.228058Z  INFO using release-plz config file release-plz.toml
2025-10-28T22:06:55.618231Z  WARN test_release_plz: failed to parse changelog at path "/home/runner/work/why_isnt_release_plz_working/why_isnt_release_plz_working/CHANGELOG.md": can't read changelog file

Caused by:
    failed to open file `/home/runner/work/why_isnt_release_plz_working/why_isnt_release_plz_working/CHANGELOG.md`: No such file or directory (os error 2). The git release body will be empty.
2025-10-28T22:06:56.072544Z  INFO published test_release_plz 0.1.0
release_output: {"releases":[{"package_name":"test_release_plz","prs":[],"tag":"v0.1.0","version":"0.1.0"}]}
```
