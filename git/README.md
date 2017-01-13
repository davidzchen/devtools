# Git configuration for Bazel

By running [install-tools](install-tools), you clone if not cloned
a Bazel repository and install the following tools:

 - A `git rb` alias to rebase on top of master with the Bazel repository,
 - A `git review` alias to send a patch set to review on gerrit,
 - Two commit hooks for adding the change id for gerrit and for applying
   buildifier to build files.
