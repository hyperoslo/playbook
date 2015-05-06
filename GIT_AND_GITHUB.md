# Git & GitHub Conventions

These conventions apply to our open-source, internal and client projects.

## Basic Setup

- [Create a GitHub account](https://github.com/join)
- [Download GitHub for Mac](https://mac.github.com/)
- Open GitHub for Mac and log in
- Visit the repository on GitHub and press “Clone to Desktop”

## Commits

For applications, the `master` branch should be in production at all times.
A `develop` branch may be used for staging purposes.

For libraries (e.g. a Ruby gem), the `master` branch is deemed unstable.

Write grammatically correct (i.e. start with a capital) commit messages in [imperative, present tense](http://stackoverflow.com/questions/3580013/should-i-use-past-or-present-tense-in-git-commit-messages).

Prefer concise commits over gigantic ones. When writing a concise commit message
is difficult, it may indicate too many unrelated changes.

Commit summaries shouldn't end with a dot. Descriptions should.

## Branches

### Naming

Branches are awesome. We use `feature`, `fix`, `improve` and `refactor`:

```
feature/my-feature
fix/make-it-work
improve/make-it-better
refactor/make-it-awesome
```

Use `--no-ff` when you merge to `master` or `develop`.

### Merging

It's okay to just push to `develop` or `master` if it's a quick fix and you really need
it out the door. Otherwise, make it a pull request.

#### Who merges the pull request?

You do! "Woa", you might say, "what's the point of making a pull request if I'm merging it
myself?". Pull requests are less about quality assurance and more about collaborating and
learning from each other for us, so as long as someone else has seen it and left their mark
(commonly a random set of any two emoji, a single :+1: or a gif) you're good to go.

Once the pull request is accepted, delete the branch.

#### Then what?

If you're working on an application and you merged to `develop` or `master`, you push it to
the staging or production server, respectively. The staging server should *always* be on the
tip of `develop` and the production server should *always* be on the tip of `master`.

If you're working on a library (e.g. a Ruby gem) and you merged to `master`, you
may want to push a new version. Or not.
