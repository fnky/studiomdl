# CONTRIBUTING

### Fork

Fork the project and check out your copy.

```
$ git clone https://github.com/fnky/studiomdl.git
$ cd studiomdl
$ git remote add upstream https://github.com/fnky/studiomdl.git
```

Now decide if you want your feature or bug fix to go into the master branch or the stable branch. As a rule of thumb, bug fixes go into the stable branch while new features go into the master branch.

In case of doubt, open an issue in the [issue tracker](https://github.com/fnky/studiomdl/issues).

### Branch

Create a feature branch and start hacking:

```
$ git checkout -b my-feature-branch -t origin/master
```

### Commit

Make sure git knows your name and email address:

```
$ git config --global user.name "J. Doe"
$ git config --global user.email "j.doe@example.com"
```

Writing good commit logs is important. A commit log should describe what changed and why. Follow these guidelines when writing one:

1. The first line should be 50 characters or less and contain a short description of the change.
2. Keep the second line blank.
3. Wrap all other lines at 72 columns.
A good commit log looks like this:

```
explaining the commit in one line

Body of commit message is a few lines of text, explaining things
in more detail, possibly giving some background about the issue
being fixed, etc etc.

The body of the commit message can be several paragraphs, and
please do proper word-wrap and keep columns shorter than about
72 characters or so. That way `git log` will show things
nicely even when it is indented.
```

The header line should be meaningful; it is what other people see when they run git shortlog or git log --oneline.

Check the output of `git log --oneline files_that_you_changed` to find out what your changes touch.

### Rebase

Use `git rebase` (not git merge) to sync your work from time to time.

```
$ git fetch upstream
$ git rebase upstream/master
```

### Push

```
git push origin my-feature-branch
```

Go to your GitHub repository and select your feature branch. Click the 'Pull Request' button and fill out the form.

If there are comments to address, apply your changes in a separate commit and push that to your feature branch. Post a comment in the pull request afterwards; GitHub does not send out notifications when you add commits.
