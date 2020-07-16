## Track upstream

Create and track upstream from local repo:

```sh
gRa --track master upstream git@github.com:sorin-ionescu/prezto.git
```

## Create branch to submit a PR to upstream

Create a branch and cherry-pich interresting commits to push to upstream through a PR:

```sh
gbc fix-something
gwR upstream/master
gcP <interresting-commit-hash>
gpc
```

Then go to Github and create a PR to upstream

## Merge upstream

Make sure master is clean with no pending modification or unpushed commit.

Create an upstream branch to merge upstream:

```sh
gco master
gfm
gbc merge-upstream
gfm upstream master
```

Compare branch with master:

```sh
gco master
gwd master merge-upstream
```

Rebase upstream branch to master if everything is ok then push:

```sh
gco master
gr merge-upstream
gp
gbx merge-upstream
```
