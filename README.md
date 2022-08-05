# NOTICE: UNMAINTAINED

This project is not maintained anymore.

Author explored the idea of storing microblog entries in git history and while
the idea still seems interesting, author has moved on and is not pursuing this
any further.

---

# Microblogging via git commit messages

Git commits are a perfect place to store microblog entries:

- Commit messages are intended for storing short pieces of text (with a heading)
- Author information and timestamp are appended automatically
- A lot of good tooling already exists for git


## A few conventions are required to turn git history into a simple (micro)blog

- **Only empty commits represent blog entries.**

  Commits which modify file tree should be ignored when rendering blogs. This
  may be useful to store related or unrelated code in the file tree.

- **Rendering settings are stored in microblog.toml file in repository**

  This file will provide information on how to render the blog: default
  markup engine, main author, etc. See [example][microblog.toml]

[microblog.toml]: https://github.com/sio/microblog-python/blob/master/microblog.toml.example

- **Extra metadata is appended to the end of commit message**

  `Key: Value` pairs are used similar to `Signed-off-by:` fields. To avoid
  confusion and simplify parsing metadata should appear only in the last lines
  of commit message and all keys should start with `Microblog-`


## Examples

- Sample blog: [read from the bottom up][sample-render], [git history][sample],
  [git repo][sample-repo]
- Rendered with: [microblog-python]

[sample-render]: https://sio.github.io/microblog-spec/#4d48088968fbbe4157baf44380b4ce1d5c03fcc6
[sample]: https://github.com/sio/microblog-spec/commits/sample
[sample-repo]: https://github.com/sio/microblog-spec/tree/sample
[microblog-python]: https://github.com/sio/microblog-python


## License and copyright

To the extent possible under law, the contributors of this repository waived
all copyright and related or neighboring rights to the files in this
repository unless otherwise noted, according to the Creative Commons CC0
license.

More information: http://creativecommons.org/publicdomain/zero/1.0/
