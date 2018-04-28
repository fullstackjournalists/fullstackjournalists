# Syncing to this repository

If you've made changes to this repository, you probably forked and cloned
it to make a local copy of your own.

But what if others have contributed changes to the `/fullstackjournalists` repository
that aren't present in your local one? How do you get back in sync?

## Upstream and downstream

If you fork and clone a repository to make your own local copy to work on or play with,
your cloned repository is "downstream." The original repository is "upstream."

For example, I forked this repository, so there's a copy at [http://github.com/lisawilliams/fullstackjournalists](http://github.com/lisawilliams/fullstackjournalists). That's my "downstream" repository

Let's say other members of the group make a change, like adding a file with
our constitution in it. Now, my local repository doesn't have that file. If I am at the
command line and type `git pull origin master`, that pulls changes from my downstream repo at
[http://github.com/lisawilliams/fullstackjournalists](http://github.com/lisawilliams/fullstackjournalists), not the upstream repo at [http://github.com/fullstackjournalists/fullstackjournalists](http://github.com/lisawilliams/fullstackjournalists), where the changes are.

So in order to `sync` my downstream repository with the upstream one, I have to do the following:

### Create a link to the upstream repository

First, I have to let my local repository know the location of the upstream repository.

In Terminal, I switch into the directory of my local repository. At the command line,
I check to see what remote repositories already exist. At the command line, I type

`git remote -v`

It should show me the url for my copy of the repository on Github, something like:

http://github.com/yourusername/yourrepositoryname.git

Let's add a link to the upstream repository on Github.

In the case of this repository, that's http://github.com/fullstackjournalists/fullstackjournalists.git.

We add a remote at the command line by typing:

`git remote add upstream http://github.com/fullstackjournalists/fullstackjournalists.git`

At the command line, type `git remote -v` again and you'll see your nifty new upstream remote.

Here's [Github's documentation on adding a link to an upstream remote repository](https://help.github.com/articles/configuring-a-remote-for-a-fork/) Github's documentation is pretty great and always worth a browse. 

### Syncing your downstream repository with the upstream one

Now git knows where the upstream repository is, we can sync. At the command line, type:

`git fetch upstream`

You will now have a new branch called `upstream/master`.

You now have a local copy of any changes and files in the upstream repository at fullstackjournalists/fullstackjournalists. (Here's Github's documentation on [syncing a remote repository](https://help.github.com/articles/syncing-a-fork/)).

However, you probably still want to `merge` those changes into your own repository.

Check out your own master branch by typing `git checkout master` at the command line.
Then, to unify your `master` branch with the changes you just fetched from the upstream
repository, type `git merge upstream/master`.

Now, your local master branch is in sync with the upstream one! 🎉

### Make changes

Now, you can make any changes you want to make, commit them, push them to your local repository, and make a pull request on the main upstream repository to contribute your changes.
