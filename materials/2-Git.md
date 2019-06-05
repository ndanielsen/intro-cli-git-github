# What is git?

Git is a free and open distributed version control system. Every developer (and others) has a working copy of the code and full change history on their local machine.

Git was created by Linus Torvalds. The first commit of git was of git itself.

### Starting a new project

Let's navigate to our ~/Desktop, create a new project and initialize git.

```

  $ cd ~/Desktop
  $ mkdir icecream_shop
  $ cd icecream_shop/
  $ git init

```

### A Little Set Up Required

We need to tell git who we are. 

```
  $ git config --global user.name "Nathan Danielsen"
  $ git config --global user.email "nathan.danielsen@gmail.com"
```

Let's check that it made it in,

```
  $ git config --global user.name
  $ git config --global user.email
```


## Most Common Workflow

### Adding a File to git

Let's create a file and store it in git.

```

  $ touch icecream.txt
  $ git add icecream.txt
  $ git status
  $ git commit -m "Added an important file"
  $ git log

```
# Exercise

- Create a file named `sauces.txt`
- Add it to git staging
- Commit it with a message
- Check that it made it in!

## Other Common Workflows

### Changing a File

Let's open up the `icecream.txt` and write the name of some flavors we like.

Now let's check git, add the file to staged to be commited and then commit it.

```

 $ git status
 $ git add icecream.txt
 $ git commit -m "Added my favorite flavors"
 $ git log

```

### Adding Multiple Files

Let's add some optional toppings that we can add to it. In each of those toppings, write in some sauce types and names of nuts.

```

 $ mkdir toppings
 $ touch toppings/nuts.txt
 $ touch toppings/sauce.txt

```

Let's now add it to git to be stored in version control.

```

  $ git add toppings
  $ git status
  $ git commit -m 'added my favorite toppings'

```


### Removing File from Staging

Sometimes we accidentally add a file(s) to be committed by mistake. We can reset them to remove them from being staged for a commit like this:

```

 $ git reset icecream.txt
 $ git status

```

## Collaboration - Sharing Your Work on Github

Now that you have a git repository with some work. Let's share our icecream shop with the world.

Let's first visit Github.com and choose to create a "New Repository" by selecting it from the plus icon in the upper right corner.

Next on the "Create a new repository" screen, let's:

- Make the respository name "ice-cream-shop"
- Press the "Create repository" Button


#### Congrats, you've created your first repository

Now let's share your icecream show with the world.

## Exercise

Follow the instructions in this section "…or push an existing repository from the command line"

## Deep Dive Into Collaboration with Git

Now that you've set up your `ice-cream-shop` repository on github, let's explore the how and why that worked.

#### What is a remote in git?

Type in your terminal: 

`git remote`

Let's use the commandline to learn a little more about `git remote`

`git remote --verbose`


### Exercise

1) Can you figure out what is the command to "show remote url after name?"
2) What is url for `origin` in your git repository?

Bonus:
3) Can you figure out how to remove and add a remote to this repository?
4) Add nathan's (ice-cream-shop)[https://github.com/ndanielsen/ice-cream-shop.git] as a remote named `ndanielsen`


#### What is `git push`?

Typical Format: `git push <remote> <branch>`

The `git push` command is used to transfer your git commits on your working branch (ie master) to a remote location such as github.

See "4-Git-Advanced.md" for more on branches.

In another sense, `git push` is used to syncronize your work on local computer with that on the github website server.

### Exercise

- Create a file named `house_special.txt`
- In that file, write down a special dessert that is contains icecream!
- Add and commit that file to git
- Send that file up to github (hint: how did you originally send up your repo to github?)

### Further Reading
- [Atlassian - git syncing](https://www.atlassian.com/git/tutorials/syncing)
- [The `Pro Git` e-book](https://git-scm.com/book/en/v2)