# treelease
can I release a tag that points to a tree?

I made some tags and pushed them:

```shell
$ git tag
t1.0
t1.1
t1.2
$ git cat-file -t t1.0
tag
$ git cat-file -t t1.0^{}
tree
$ git push --tags
```

GitHub says “3 releases” on the repository home page, but the [releases
page] and [tags page] are both empty.

[releases page]: https://github.com/wchargin/treelease/releases
[tags page]: https://github.com/wchargin/treelease/tags

I made some more tags and pushed them:

```shell
$ git tag metatag -m 'Tag of tag' t1.0
$ git tag b1.0 -m 'Tag of tag' t1.0
$ git tag b1.0 -m 'First version of README' HEAD^:README.md
$ git tag b2.0 -f -m 'Second version of README' HEAD:README.md
$ git tag v1.0 -m 'The very beginning' HEAD^
$ git tag vv1.0 -m 'The very beginning' HEAD^
$ git tag vv1.0 -m "You're it" v1.0
$ git tag
b1.0
b2.0
metatag
t1.0
t1.1
t1.2
v1.0
vv1.0
$ git push --tags
```

Now <./releases> 404s in the GitHub UI. :-(
