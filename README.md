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
