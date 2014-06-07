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

Use `--no-ff` when you merge to `master` or `develop`.

## Do I make a pull request or no?

* If is a quick fix: **no**
* The rest of the cases is *highly* recommended

## Who merges the pull request I just created?

Let's say you're working on a pull request. The tests are green and you're ready
to merge. Who does that? Basically anyone. Just not you.

## What do I do after merging?

If you're working on an application and you merged to `develop` or `master`, you push it to
the staging or production server, respectively. The staging server should *always* be on the
tip of `develop` and the production server should *always* be on the tip of `master`.

If you're working on a gem and you merged to `master`, you may want to push a new
version. Or not.
