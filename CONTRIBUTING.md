# Contributing to AASF IIITM Projects

Thanks for your interest in improving the projects! This document provides a step-by-step guide for general contributions to AASF IIITM porjcets.

## Communications

Before starting work on something major, please reach out to us via GitHub, email, etc. We will make sure no one else is already working on it and ask you to open a GitHub issue. Also, we will provide necessary guidance should you need it.


## Ways to Contribute

1.  **Replying and handling open issues.**  You can help out by guiding people through the process of filling out the issue template, help them in clarifying information related to code, features or bugs.
2.  **Find bugs and raise issues**  The project is in its early stage and we appreciate if you can test and find out bugs that can help us improve user experience by a manifold. Help us by creating issues for bugs you find
3.  **Suggest features**  Want something more from the project? Go ahead and create an issue suggesting us your awesome feature!
4. **Get down to coding!** We have some open issues, ranging from bugs to enhancements that we would appreciate if you could help us with.


## Submitting a PR

If you have a specific idea of a fix or update, follow these steps below to submit a PR:

- [Step 1: Setup the Repo](#step-1-setup-the-repo)
- [Step 2: Make the change](#step-2-make-the-change)
- [Step 3: Commit and push your changes](#step-3-commit-and-push-your-changes)
- [Step 4: Create a pull request](#step-4-create-a-pull-request)
- [Step 5: Get a code review](#step-5-get-a-code-review)

### Step 1: Setup the Repo

1. Fork the project repo, and then clone it:

   ```bash
   $ export user={your github. profile name}
   $ git clone git@github.com:${user}/<repo-name>.git
   ```
   or
   ```bash
   $ export user={your github. profile name}
   $ git clone https://github.com/${user}/<repo-name>.git
   ```

2. Set your cloned local to track the upstream repository:

   ```bash
   $ cd <repo-name>
   $ git remote add upstream https://github.com/AASF-IIITM/<repo-name>.git
   ```

3. Disable pushing to upstream master:

   ```bash
   $ git remote set-url --push upstream no_push
   $ git remote -v
   ```

   The output should look like:

   ```bash
   origin    git@github.com:$(user)/<repo-name>.git (fetch)
   origin    git@github.com:$(user)/<repo-name>.git (push)
   upstream  https://github.com/AASF-IIITM/<repo-name> (fetch)
   upstream  no_push (push)
   ```
   or 
   
   ```bash
   origin https://github.com/$(user)/<repo-name>.git (fetch)
   origin https://github.com/$(user)/<repo-name>.git (push)
   upstream  https://github.com/AASF-IIITM/<repo-name> (fetch)
   upstream  no_push (push)
   ```

4. Get your local master up-to-date and create your working branch:

   ```bash
   $ git fetch upstream
   $ git checkout master
   $ git rebase upstream/master
   $ git checkout -b myfeature
   ```
   
### Step 2: Make the change
  
1. Make changes which you want 
2. Follow  specific contributing guideline related to particular project
   
   
   
### Step 3: Commit and push your changes

If your project contain some test cases, please run before commiting.

1. Run the following commands to keep your branch in sync:

   ```bash
   $ git fetch upstream
   $ git rebase upstream/master
   ```

2. Commit your changes:

   ```bash
   $ git add -A
   $ git commit --signoff
   ```

3. Push your changes to the remote branch:

   ```bash
   $ git push -f origin myfeature
   ```
   
   #### Points to be noted:

      - Please have meaningful commit and PR messages.
      - Commit messages have to be in imperative tense. An example is "fix segmentation error" or "implement binary search in c++". All commit messages have to be in lower case.
      - Same is the case with Pull Requests. Pull requests have a title and a description. Title has to be short and informative.

### Step 4: Create a pull request

1. Visit your fork at <https://github.com/$user/<repo-name>> (replace \$user with your name).
2. Click the Compare & pull request button next to your `myfeature` branch.
3. Edit the description of the pull request to match your changes.

### Step 5: Get a code review

Once your pull request has been opened, it will be assigned to at least two reviewers. The reviewers will do a thorough code review of correctness, bugs, opportunities for improvement, documentation and comments, and style.

Commit changes made in response to review comments to the same branch on your fork.

