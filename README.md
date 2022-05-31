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
  markup engine, main author, etc. See [example](./microblog.toml)

- **Extra metadata is appended to the end of commit message**

  `Key: Value` pairs are used similar to `Signed-off-by:` fields. To avoid
  confusion and simplify parsing metadata should appear only in the last lines
  of commit message and all keys should start with `Microblog-`


## License and copyright

To the extent possible under law, the contributors of this repository waived
all copyright and related or neighboring rights to the files in this
repository unless otherwise noted, according to the Creative Commons CC0
license.

More information: http://creativecommons.org/publicdomain/zero/1.0/
