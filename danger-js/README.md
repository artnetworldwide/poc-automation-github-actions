# Run Danger JS Pull Request Checks

A GitHub action that will perform quality control checks on Pull Requests, according to the code specified in `./dangerfile.ts`

> A real world example: https://github.com/artsy/emission/blob/master/dangerfile.ts

```
workflow "Run Danger JS" {
  on = "pull_request"
  resolves = "danger"
}

action "danger" {
  uses = "artnetworldwide/poc-automation-github-actions/danger-js@master"
  secrets = ["GITHUB_TOKEN"]
}
```
