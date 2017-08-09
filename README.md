# Proof of concept for reddit user esbenab

The question was something along the lines of "How do I sum up who most often touch which files".

The purpose seems to be some analysis regarding who intelectually owns pieces of code within a repository.

I'm a component lover, so for me it seems like there is a monolith to be broken down :)

## The git command

You can try and run this command in any repository, and it will give a list of commits, with short-sha, author-name and then sum what files were affected by this commit.

This information could be used in a script to populate the intellectual overview database.

`git log --name-status --pretty="%h(%an) - %n"`

`git log` gives us a list of the commits on the current branch we are on.
We could add a `--all` to see history from all branches, but don't get me started on long lived branches.

`--name-status` prints out for each commit what files where affected and how.

`--pretty="%h(%an) - %s"` gives us the shortsha(%h) the authorname (%an) and the commit message subject (%s). This should be enough information for us to script our way out of our trouble, just as we like it.

Enjoy :)

/RandomSort

