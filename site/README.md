# Pushing changes for Bazel sites

This directory contains tools for pushing changes to the Bazel www and blog
sites.

## Prerequisites

Make sure you have the `gsutil` tool from the Cloud SDK installed on your
system.

## Pushing `www.bazel.build`

Clone the `bazelbuild/bazel-website` repository:

```sh
git clone git@github.com:bazelbuild/bazel-website && cd bazel-website
```

Build the site tarball:

```sh
bazel build //:jekyll-tree
```

Push to GCS:

```sh
/path/to/devtools/publish-site.sh bazel-bin/jekyll-tree.tar www.bazel.build
```

## Pushing `blog.bazel.build`

Clone the `bazelbuild/bazel-blog` repository:

```sh
git clone git@github.com:bazelbuild/bazel-blog && cd bazel-blog
```

Build the site tarball:

```sh
bazel build //:jekyll-tree
```

Push to GCS:

```sh
/path/to/devtools/publish-site.sh bazel-bin/jekyll-tree.tar blog.bazel.build
```
