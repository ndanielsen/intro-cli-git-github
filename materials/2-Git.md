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


## Advanced

### Creating a branch

Often, we might be working with others but don't want to step on each others toes and cause conflicts. In git, we use branches to work in parallel and then merge our code together.

```

 $ git branch
 $ git branch add-some-gelato
 $ git branch
 $ git checkout add-some-gelato
 $ git branch
 $ touch gelato.txt
 $ git add gelato.txt
 $ git status
 $ git commit -m 'adding gelato to the shop'

```


### Merge A Branch

Now that we have added some gelato in a separate branch (body of work) of our code, let's merge it into the master branch.

```
 $ git checkout master
 $ git merge add-some-gelato
 $ ls

```


### Resources

Here are a few other resources that might be helpful for diving deeper into git.


The `Pro Git` e-book
`https://git-scm.com/book/en/v2`

What is a commit?
`https://chris.beams.io/posts/git-commit/`
