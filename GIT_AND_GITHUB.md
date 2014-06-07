# Git & GitHub conventions

When working on a project as a Company we use the following *Git & GitHub* conventions

## Basic setup

A typical project in *Hyper* has a `master` branch, which always is production ready
and in some cases a `develop` branch when using a **Staging** server

## Branches

### Naming

Branches are awesome

The naming convention is:

```
feature/my-feature
fix/make-it-work
refactor/make-it-pretty
```

Use `--no-ff` when you merge to `master` or `develop`.

### Merging

It's okay to just push to `develop` or `master` if it's a quick fix and you really need
it out the door. Otherwise, make it a pull request.

#### Who merges the pull request?

Let's say you're working on a pull request. The tests are green and you're ready
to merge. Who does that? Basically anyone. Just not you.

#### Then what?

If you're working on an application and you merged to `develop` or `master`, you push it to
the staging or production server, respectively. The staging server should *always* be on the
tip of `develop` and the production server should *always* be on the tip of `master`.

If you're working on a gem and you merged to `master`, you may want to push a new
version. Or not.
