
# Advanced 

## Git Branches

A branch represents a different line or work that is separated from the `main` or `master` branch. It is a helpful mechanism for allowing multiple people to work on the same git repository (and github project) in potentially overlapping locations without stepping on too many toes.

In git, we use branches to work in parallel and then merge our code together.



Check out your current branch for your `ice-cream-shop` project.

```
 $ git branch
```

You should only have the master branch.


### Creating a branch

Let's create a branch to add in some gelato to our iceceam shop.

```
 $ git branch add-some-gelato
 $ git branch

```

Let's now move into that branch and add a file named 'gelato.txt'

```
 $ git checkout add-some-gelato
 $ git branch
 $ touch gelato.txt
 $ git add gelato.txt
 $ git status
 $ git commit -m 'adding gelato to the shop'

```

Exercise:
1) Let's `push` these changes up to our github for this.
hint: `git push <origin> <branch_name>`
2) Checkout your github `ice-cream-shop` repo to make sure that it made it.
3) On github, make a pull request into your `master` branch and then merge it in.

#### Protip: 
You can create and checkout a branch in one command.
```
 $ git checkout -b some-branch`
```



### Pulling Down a Branch

Now that we have an updated `master` branch. Let's get the same copy of it on our local computer

```
 $ git checkout master
 $ git pull

```

Exercise:
1) How can you confirm that your gelato commits have made it down?
2) Can you figure out how to delete your old branch `add-some-gelato`? 
hint: `git branch --help`


### Merge A Branch

Now that we have added some gelato in a separate branch (body of work) of our code, let's merge it into the master branch.

```
 $ git checkout master
 $ git merge add-some-gelato
 $ ls

```

### Resources

Here are a few other resources that might be helpful for diving deeper into git.

- [What is a commit?](https://chris.beams.io/posts/git-commit/)
- [Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials)

