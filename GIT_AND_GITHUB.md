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

Pull request descriptions should be concise and well written. The merger should
be able to copy this description straight into the release notes instead of
figuring out what changed or was fixed. 

#### Who merges the pull request?

Core contributors have the final say on what gets merged into their codebase,
so they get to click the button. That could be you, but if you're working with
someone else it should probably be them. The important thing is that someone else
gets to look it over so we can learn from you, point out your silly mistakes and/or
post the sufficient amount of gifs.

Once the pull request is accepted, the person who merged should delete the branch.

#### I need the code in my last pull request in my next. What do?

If your next pull request is intimately related to your last, consider to
continue working on the one pull request instead of opening another.

If you'd really rather open another, it's okay to base your next pull request
from your unmerged branch. Request that it be merged to the main branch,
though, and be sure to merge any changes you've made to its parent during
its review.

#### Then what?

If you're working on an application and you merged to `develop` or `master`, you push it to
the staging or production server, respectively. The staging server should *always* be on the
tip of `develop` and the production server should *always* be on the tip of `master`.

If you're working on a library (e.g. a Ruby gem) and you merged to `master`, you
may want to push a new version. Or not.
