# Git & GitHub conventions

When working on a project as a Company we use the following *Git & GitHub* conventions

## Basic setup

A typical project in *Hyper* has a `master` branch, which always is production ready
and in some cases a `develop` branch when using a **Staging** server

## Branch out!

Branches are awesome

The naming convention is:

```
feature/my-feature
fix/make-it-work
refactor/make-it-pretty
```

## Do I make a pull request or no?

* If is a quick fix: **no**
* The rest of the cases is *highly* recommended

## Who merges the pull request I just created?

Asuming that you finish working on a pull request and all the test are green, then depending on the branch:

* To `master` always someone else should merge the pull request
* To a development branch you can merge the pull request if you want
