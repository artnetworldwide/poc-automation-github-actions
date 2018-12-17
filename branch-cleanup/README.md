# Branch Cleanup Action

A GitHub action to automatically delete the branch after a pull request has been merged.

> **NOTE:** This will **never** delete the repository's default branch. If the pull request is closed _without_ merging, it will **not** delete it.

```
workflow "on pull request merge, delete the branch" {
  on = "pull_request"
  resolves = ["branch-cleanup"]
}

action "branch-cleanup" {
  uses = "artnetworldwide/poc-automation-github-actions/branch-cleanup@master"
  secrets = ["GITHUB_TOKEN"]
}
```
