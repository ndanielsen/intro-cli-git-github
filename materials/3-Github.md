# What is Github?

 GitHub is a website and cloud-based service that allows developers to store and collaborate with others on codebases and projects. It allows them to easily track and control changes to their code.

## Getting Started on GitHub

The lesson materials are hosted on GitHub at https://github.com/ndanielsen/intro-cli-git-github.


## Typical Workflows on Github

The typical workflow for a contributor to a new `Hack for La` Project is as follows:

1. **Discover** a bug or a feature.
2. **Discuss** with the project leads by [adding an issue](https://github.com/ndanielsen/intro-cli-git-github/issues).
3. **Assign** yourself the task by pulling a card from the Issues [Issues](https://github.com/ndanielsen/intro-cli-git-github/issues).
4. **Fork** the repository into your own GitHub account.
5. Create a **Pull Request** first thing to [connect with them](https://github.com/ndanielsen/intro-cli-git-github/pulls) about your task.
6. **Code** the feature, write the documentation, add your contribution.
7. **Review** the code with the Project Leads who will guide you to a high quality submission.
8. **Merge** your contribution into the intro-cli-git-github codebase.

**Note**: Create a pull request as soon as possible, even before you've started coding. This will allow the Project Leads to give you advice about where to add your code or utilities and discuss other style choices and implementation details as you go. Don't wait!

Many Hack-for-La projects believe that *contribution is collaboration* and therefore emphasize *communication* throughout the entire process. Project Leads rely heavily on GitHub's social coding tools to allow them to do this.

### Forking the Repository

The first step is to fork the repository into your own account. This will create a copy of the codebase that you can edit and write to. Do so by clicking the **"fork"** button in the upper right corner of the GitHub page.

Once forked, use the following steps to get your development environment set up on your computer.

#### Clone the repository

  After clicking the fork button, you should be redirected to the GitHub page of the repository in your user account. You can then clone a copy of the code to your local machine.

  ```
  $ git clone https://github.com/[YOURUSERNAME]/intro-cli-git-github
  $ cd intro-cli-git-github
  ```

#### Pushing Up Commits to Github

  To share the commits and changes that you've made to your codebase on you github, you need to **push** up your changes.

  ```
  $ git add <your-files>
  $ git commit -m 'changes have been made'
  $ git push origin master
  ```

# Wrap Up Exercise

### What is Your Secret Power?

As a final test of your prowess with the command line, git, and github - please contribute what your secret power would be in a text file.

You will also listed as a contributor to this workshop - thus making your first open source contribution.

#### Instruction
- Make a comment in the issue: [Need List of Secret Powers](https://github.com/ndanielsen/intro-cli-git-github/issues/2)
- Fork the `intro-cli-git-github` code repository on github.
- Clone your `fork` on this repo onto your local machine.
- Create a file with your github name in `contributors/` (for example: `contributors/ndanielsen.txt`)
- In that newly created file, write in what your secret power would be.
- Commit and push that up to your repository on github.
- Create a pull-request with that file into the workshop repository.

### Extra Credit
- Instead of a text file, create a [markdown document](https://guides.github.com/features/mastering-markdown/) instead.


#### Resources

[Hello World In Github](https://guides.github.com/activities/hello-world/)
[Mastering Markdown](https://guides.github.com/features/mastering-markdown/)